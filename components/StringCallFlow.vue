<script setup lang="ts">
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'

// Step-driven animation for page 9; total steps set by `clicks: 5` in the slide frontmatter.
const { $clicks } = useSlideContext()
const step = computed(() => $clicks.value)

const code = [
  '<k>def</k> <f>double</f>(x) = x * <n>2</n>',
  '',
  'i = <n>0</n>; sum = <n>0</n>',
  '<k>while</k> i &lt; <n>200_000_000</n>',
  '  sum += <f>double</f>(i)',
  '  i += <n>1</n>',
  '<k>end</k>',
  '<f>puts</f> <f>double</f>(<s>"ab"</s>)  <c># ← new!</c>',
]
// lines (1-based) highlighted at each step
const highlight = [[], [8], [1, 5, 8], [1], [5], [4, 5, 6, 7]]

// slot boxes at `from` step
const slots = [
  { name: 'x', where: 'param of double', from: 2 },
  { name: 'double(…)', where: 'return value', from: 3 },
  { name: 'sum', where: 'local variable', from: 4 },
]
const ops = [
  { name: 'x * 2', fast: 'add 2 (inlined)', slow: 'sp_poly_mul()', from: 2 },
  { name: 'sum += …', fast: 'C int add', slow: 'sp_poly_add()', from: 4 },
]

const captions = [
  'Integer only: every slot is a plain C integer. The C compiler inlines <code>double</code>.',
  'Add <b>ONE</b> line after the loop. It runs only <b>once</b>…',
  '① Call sites merge: <code>x</code> now gets Integer <b>and</b> String → <b>boxed</b>. <code>x * 2</code> must check the tag at runtime.',
  '② So <code>double</code> may return Integer <b>or</b> String → its return is boxed too.',
  '③ <code>sum += double(i)</code> receives a boxed value → <code>sum</code> is boxed; <code>+=</code> becomes a runtime call.',
  '④ Back in the loop: <b>every</b> iteration now pays 2 runtime calls + tag checks — × 200,000,000.',
]
</script>

<template>
  <div class="scf">
    <div class="scf-code">
      <div
        v-for="(line, i) in code" :key="i"
        class="scf-line"
        :class="{ hl: highlight[Math.min(step, 5)].includes(i + 1), hidden: i === 7 && step < 1, dim: highlight[Math.min(step, 5)].length && !highlight[Math.min(step, 5)].includes(i + 1) }"
      >
        <span class="ln">{{ i + 1 }}</span><span v-html="line || '&nbsp;'" />
      </div>
    </div>

    <div class="scf-right">
      <div class="scf-label">Type slots</div>
      <div class="scf-slots">
        <div v-for="s in slots" :key="s.name" class="slot" :class="{ boxed: step >= s.from }">
          <code>{{ s.name }}</code>
          <small>{{ s.where }}</small>
          <span class="ctype">{{ step >= s.from ? 'sp_RbVal (boxed)' : 'sp_int' }}</span>
        </div>
      </div>

      <div class="scf-label">Operations</div>
      <div class="scf-ops">
        <div v-for="o in ops" :key="o.name" class="op" :class="{ boxed: step >= o.from }">
          <code>{{ o.name }}</code><span>→</span><code class="ctype">{{ step >= o.from ? o.slow : o.fast }}</code>
        </div>
      </div>

      <div class="scf-cost" :class="{ boxed: step >= 5 }">
        <template v-if="step < 5">Per iteration: <b>~8 instructions, 0 calls</b></template>
        <template v-else>Per iteration: <b>2 calls + tag checks</b> → <span class="big">~15× slower</span></template>
      </div>
    </div>

    <div class="scf-caption">
      <span class="dots"><i v-for="n in 6" :key="n" :class="{ on: n - 1 <= step }" /></span>
      <span v-html="captions[Math.min(step, 5)]" />
    </div>
  </div>
</template>

<style scoped>
.scf { display: grid; grid-template-columns: 1fr 1fr; gap: 1.2rem 1.6rem; margin-top: .4rem; }
.scf-code { background: #1e1c2e; color: #e6e1f0; border-radius: 10px; padding: .9rem .6rem; font-family: 'Fira Code', monospace; font-size: .82rem; }
.scf-line { padding: .12rem .5rem; border-radius: 4px; transition: all .4s; white-space: pre; }
.scf-line .ln { display: inline-block; width: 1.6rem; color: #6b6585; }
.scf-line.hl { background: rgba(189, 63, 50, .45); }
.scf-line.dim { opacity: .45; }
.scf-line.hidden { opacity: 0; }
.scf-line :deep(k) { color: #ff7b9c; }
.scf-line :deep(f) { color: #82d9a0; }
.scf-line :deep(n) { color: #f7c46c; }
.scf-line :deep(s) { color: #ffb38a; text-decoration: none; }
.scf-line :deep(c) { color: #fff59d; }

.scf-label { font-size: .68rem; text-transform: uppercase; letter-spacing: .08em; color: var(--rt-grey); margin: .2rem 0 .3rem; }
.scf-slots { display: grid; grid-template-columns: repeat(3, 1fr); gap: .5rem; }
.slot, .op, .scf-cost { border: 2px solid #3aa364; background: #effaf3; border-radius: 8px; transition: all .45s; }
.slot { padding: .45rem .5rem; text-align: center; }
.slot code { display: block; font-weight: 600; font-size: .85rem; background: none; }
.slot small { display: block; font-size: .6rem; color: #777; }
.ctype { font-family: 'Fira Code', monospace; font-size: .68rem; color: #2a7a4a; }
.scf-ops { display: flex; flex-direction: column; gap: .4rem; }
.op { display: flex; gap: .5rem; align-items: center; padding: .3rem .6rem; font-size: .8rem; }
.op code { background: none; }
.boxed { border-color: var(--rt-red); background: #fdecea; }
.boxed .ctype { color: var(--rt-red); font-weight: 600; }
.scf-cost { margin-top: .6rem; padding: .5rem .7rem; font-size: .85rem; }
.scf-cost .big { color: var(--rt-red); font-weight: 700; font-size: 1.15rem; }

.scf-caption { grid-column: 1 / -1; display: flex; gap: .8rem; align-items: center; font-size: .95rem; border-top: 1px solid #eee; padding-top: .6rem; min-height: 3.2rem; }
.scf-caption :deep(code) { font-size: .85rem; }
.dots { display: flex; gap: .25rem; flex-shrink: 0; }
.dots i { width: .5rem; height: .5rem; border-radius: 50%; background: #ddd; transition: background .3s; }
.dots i.on { background: var(--rt-red); }
</style>
