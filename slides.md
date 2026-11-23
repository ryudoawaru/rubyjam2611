---
theme: default
colorSchema: light
title: "What's Spinel? — Ruby Jam Nov 2026"
author: Ruby Taiwan
aspectRatio: 16/9
canvasWidth: 980
duration: 13min
transition: fade
drawings:
  enabled: false
fonts:
  provider: none
layout: cover
class: p-0
---

<div class="rt-red-bg flex flex-col items-center justify-center text-center gap-4">
  <img src="/ruby_taiwan_logo.svg" class="w-28" />
  <h1 class="lobster !text-white !text-8xl !font-normal !m-0">Ruby Jam</h1>
  <p class="text-3xl font-bold !m-0 !opacity-100">Nov 24, 2026</p>
  <p class="text-xl opacity-90">Ruby Taiwan monthly meetup</p>
  <img src="/ruby_taiwan_logotype.svg" class="w-56 mt-6" style="filter: brightness(0) invert(1)" />
</div>

<!--
[0:00–0:20]
大家好，歡迎來到 11 月的 Ruby Jam！
開始之前，先跟大家講一下今晚的流程、贊助商，還有幾個近期的活動。
-->

---

# Tonight

| Time | Session |
|---|---|
| 19:30 | **Hello, Spinel: The New Ruby AOT Compiler!** — Aotokitsuruya |
| 20:10 | **Rails Beginner, Big Adventure! My First Kaigi on Rails!** — Vevila |
| 20:50 | **Open Discussion** — OSS contribution, problem solving, sharing |

<!--
[0:20–0:40]
快速看一下今晚流程：
- 7:30 Aotokitsuruya 講 Spinel，會有 live demo（麥克風 + Whisper 語音轉字幕，打包成單一執行檔）
- 8:10 Vevila 分享第一次參加 Kaigi on Rails 的心得，Rails 新手一定有共鳴
- 8:50 開放討論
-->

---

# Thanks to our sponsors 💎

<div class="stats" style="grid-template-columns: repeat(2, 1fr)">
  <div class="stat">
    <div class="flex items-center justify-center gap-4 h-24 mb-3">
      <img src="/logo_piccollage.png" class="h-24 mix-blend-multiply" />
      <div class="text-3xl red font-bold">×</div>
      <img src="/logo_day1.svg" class="h-20 rounded mix-blend-multiply" />
    </div>
    <b class="!text-xl">PicCollage × Day1 Coworking Space</b><span class="!text-lg">Venue</span>
  </div>
  <div class="stat">
    <div class="flex items-center justify-center h-24 mb-3"><img src="/logo_5xruby.svg" class="h-20" /></div>
    <b class="!text-xl">5xRuby</b><span class="!text-lg">Food</span>
  </div>
</div>

<!--
[0:40–0:55]
感謝今晚的贊助商：
PicCollage 和 Day1 Coworking Space 提供場地，
5xRuby 贊助今天的食物，大家吃飽一點！
-->

---

<div class="flex items-center gap-6">
  <img src="/rwc_hero.svg" class="h-32" />
  <div>
    <h1 class="!mb-1">RubyWorld Conference 2026</h1>
    <p class="text-xl !m-0">Dec 3–4 (Thu–Fri) · Kunibiki Messe, Matsue, Shimane 🇯🇵</p>
  </div>
</div>

<div class="grid grid-cols-2 gap-4 mt-5">
  <div class="stat flex items-center gap-4 !text-left">
    <img src="/rwc_irina.jpg" class="w-20 h-20 rounded-full object-cover" />
    <div><b class="!text-xl">Ruby Startups Today</b><span class="block">Irina Nazarova · CEO, Evil Martians</span><span class="block">Keynote · Day 1</span></div>
  </div>
  <div class="stat flex items-center gap-4 !text-left">
    <img src="/rwc_matz.jpg" class="w-20 h-20 rounded-full object-cover" />
    <div><b class="!text-xl">Extreme Vibe Coding</b><span class="block">Yukihiro “Matz” Matsumoto</span><span class="block">Keynote · Day 2</span></div>
  </div>
</div>

<div class="mt-4"></div>

- **Day 1** also hosts the **Ruby Prize** & **Ruby biz Grand prix** awards →
- Registration extended to <span class="red font-bold">Nov 30 (Mon)</span> · 2026.rubyworld-conf.org

<!--
[0:55–1:30]
順便宣傳一下：下週 12/3–4 就是 RubyWorld Conference 2026，在島根松江的くにびきメッセ。
兩場 Keynote：第一天是 Evil Martians CEO Irina Nazarova 講「Ruby Startups Today」，
第二天是 Matz 本人，題目是「エクストリームバイブコーディング」——Extreme Vibe Coding，
剛好跟今天的 Spinel 有點呼應，Matz 最近怎麼寫程式，可以現場聽他講。
報名延長到 11/30（一），報完不能取消，有興趣的朋友這週快決定！
第一天還有兩個頒獎，接下來兩頁各別介紹。
-->

---

<div class="flex items-end gap-4">
  <img src="/rwc_ruby_prize.jpg" class="h-20 mix-blend-multiply" />
  <span class="text-5xl font-bold red mb-2">2026</span>
</div>

<p class="text-lg mt-2">Honors <b>individuals</b> with notable recent contributions to the Ruby community · winner gets <span class="mark">¥1,000,000</span> from Matsue City · awarded at RWC</p>

<p class="muted !mb-1">Final nominees</p>
<div class="grid grid-cols-3 gap-3">
  <div class="stat flex items-center gap-3 !text-left !p-3">
    <img src="/rb/prize_yudai-takada.jpg" class="w-16 h-16 rounded-full object-cover" />
    <div><b class="!text-lg">Yudai Takada</b><span class="block">Regional RubyKaigis &amp; local .rb groups</span></div>
  </div>
  <div class="stat flex items-center gap-3 !text-left !p-3">
    <img src="/rb/prize_satoshi-tagomori.jpg" class="w-16 h-16 rounded-full object-cover" />
    <div><b class="!text-lg">Satoshi Tagomori</b><span class="block">Brought Ruby::Box into Ruby 4.0</span></div>
  </div>
  <div class="stat flex items-center gap-3 !text-left !p-3">
    <img src="/rb/prize_marco-roth.jpg" class="w-16 h-16 rounded-full object-cover" />
    <div><b class="!text-lg">Marco Roth</b><span class="block">Ruby dev tooling (Herb, …) &amp; RubyEvents.org</span></div>
  </div>
</div>

<p class="mt-5">Last year's winner: <b>Stan Lo</b> 🇹🇼 — author of <span class="muted">st0012.dev/spinel</span>, the main source for this talk</p>

<p class="muted text-sm">Source: rubyprize.jp</p>

<!--
[1:30–1:55]
第一個是 Ruby Prize，由 Matz 擔任實行委員長，表彰「個人」在近幾年對 Ruby 社群的貢獻，
得主可以拿到松江市提供的 100 萬日圓獎金，在 RubyWorld 上頒獎。
今年的最終候選有三位：
- 高田雄大：辦了很多地域 Ruby 會議和地域 .rb，在関ケ原 RubyKaigi 辦了 RubyKaja
- 田籠聡（tagomoris）：把 Ruby::Box 帶進 Ruby 4.0
- Marco Roth：Herb 等 Ruby 開發工具，還有 RubyEvents.org
特別提一下：去年 2025 的得主是 Stan Lo（羅泓武），
就是今天這份 Spinel 介紹主要參考的那篇文章作者！
-->

---
layout: cover
class: p-0
---

<div class="w-full h-full flex items-center justify-center" style="background:#121115">
  <div class="relative">
    <img src="/rb/finalist.png" class="block" style="height:551px" />
    <!-- SOSI card outline, % of the screenshot (measured on the 2x PNG) -->
    <div class="absolute" style="left:50.75%; top:29.09%; width:21.1%; height:30.38%; outline:4px solid #fff59d; outline-offset:3px"></div>
    <p class="absolute right-[5%] top-[7%] text-right text-white text-base leading-normal !m-0">
      Award ceremony <b>Dec 3 (Thu) 17:00</b> · Kunibiki Messe<br>
      Grand prix ×~2 (<b>¥1M</b>) · Special award ×~3 (<b>¥300k</b>)<br>
      <span class="opacity-60 text-xs">19 entries · judging chair: Matz · source: rubybiz.jp</span>
    </p>
  </div>
</div>

<!--
[1:55–2:20]
第二個是 Ruby biz Grand prix，表彰「用 Ruby 把生意做起來」的企業和服務，評審委員長也是 Matz。
今年 19 件報名、選出 7 件入圍：レポサク、スクールタクト、SOSI、Teachme Biz、Akerun、リーナー見積、モチベーションクラウド。
最後會選出約 2 件大賞（各 100 萬日圓）和約 3 件審查員特別賞（各 30 萬日圓），
12/3 下午五點在くにびきメッセ頒獎，也有線上直播。
小小業配：5xRuby 的 SOSI 也入圍了 🎉 結果出爐再跟大家分享！
-->

---
layout: cover
class: p-0
---

<div class="rt-red-bg flex flex-col items-center justify-center text-center gap-4">
  <p class="lobster text-3xl opacity-90">Next Ruby Jam</p>
  <h1 class="!text-white !text-6xl !font-bold !m-0">Dec 17, 2026 (Thu)</h1>
  <p class="text-2xl opacity-80 mt-4">Topics TBA — stay tuned!</p>
</div>

<!--
[2:20–2:30]
下一場 Ruby Jam 是 12/17（四），內容還在規劃中，確定後會在社群公布。
-->

---
layout: cover
class: p-0
---

<div class="rt-red-bg flex flex-col items-center justify-center text-center gap-4">
  <img src="/ruby_taiwan_logo.svg" class="w-28" />
  <p class="lobster text-2xl opacity-90">Ruby Jam · Nov 24, 2026</p>
  <h1 class="!text-white !text-6xl !font-bold !m-0">What's Spinel?</h1>
  <p class="text-xl opacity-90">A quick primer on Matz's Ruby compiler</p>
  <img src="/ruby_taiwan_logotype.svg" class="w-56 mt-6" style="filter: brightness(0) invert(1)" />
</div>

<!--
[2:30–2:50]
好，回到今晚的主題。
今晚第一場是 Aotokitsuruya 的 Spinel 深度分享。
在那之前，我先用 7 分鐘幫大家做個「Spinel 是什麼」的科普，
特別是剛開始學 Rails 的朋友，聽完後面的演講會比較好跟上。
-->

---

# How Ruby runs today

<div class="pipe flow3">
<div class="col">
<div class="step">app.rb<small>your source</small></div>
<div v-click class="card">

```ruby
def double(x) = x * 2

puts double(21)
```

</div>
</div>
<div class="arrow">→</div>
<div class="col">
<div class="step">Bytecode<small>at load time</small></div>
<div v-click class="card">
<p class="cap"><code>ruby --dump=insns app.rb</code></p>

```text
# inside double (main omitted)
getlocal   x
putobject  2
opt_mult         # x * 2
leave
```

</div>
</div>
<div class="arrow">→</div>
<div class="col">
<div class="step hot">CRuby VM<small>interpreter (+ YJIT)</small></div>
<div v-click class="card">
<p class="cap"><code>opt_mult</code> → <code>vm_opt_mult()</code></p>

```c
if (FIXNUM_2_P(recv, obj) &&
    /* Integer#* not redefined */)
  return rb_fix_mul_fix(recv, obj);
else if (/* both Float, not redefined */)
  return DBL2NUM(f1 * f2);
else
  return Qundef; // → normal method call
```

<p class="cap">Checks types on <b>every</b> <code>*</code></p>
</div>
</div>
</div>

<p class="text-sm mt-4">Runs while it reads → <code>eval</code>, <code>method_missing</code>, <code>define_method</code> work (Rails magic ✨) · but users need <b>Ruby installed</b></p>

<!--
[2:50–4:00]
先講我們平常怎麼跑 Ruby。你打 ruby app.rb 或 rails s，背後是 CRuby（也叫 MRI）。
我們用等一下 Spinel 也會用到的同一個例子：double(x) = x * 2。

[click] 第一步是你寫的原始碼，就這兩行。

[click] CRuby 載入檔案時，先把它編成 YARV bytecode——一種給 VM 看的指令。
大家可以自己試：ruby --dump=insns app.rb。
double 裡面就四條指令：取出 x、放進 2、opt_mult（也就是 x * 2）、回傳。
注意 bytecode 裡沒有寫 x 是什麼型別——因為 CRuby 在這時候也不知道。

[click] 然後 VM（用 C 寫的直譯器）一條一條執行這些指令。
opt_mult 對應到 CRuby 原始碼裡的 vm_opt_mult：
兩邊都是 Integer、而且沒人重新定義 Integer#* → 走快速的整數乘法；
兩邊都是 Float → 浮點乘法；
其他情況（例如字串）→ 回傳 Qundef，改走一般的方法呼叫，去找 String#*。
重點：每一次執行 x * 2，VM 都要先檢查型別。等一下第 8 頁會看到，Spinel 的 sp_poly_mul 做的是同一件事——差別是 Spinel 只在型別混在一起時才需要。

也因為是「邊跑邊解讀」，Ruby 可以在執行期間才產生新的程式碼——eval、method_missing、define_method，這些就是 Rails 魔法的來源。
代價是：要跑你的程式，對方電腦一定要裝 Ruby。
（YJIT 是 JIT，執行中再把熱點編成機器碼，但本質上還是在 VM 裡。）
-->

---

# Enter Spinel

**An ahead-of-time (AOT) compiler for Ruby** — by **Matz**, first commit Mar 16, 2026

<div class="pipe">
  <div class="step">app.rb<small>whole program</small></div><div class="arrow">→</div>
  <div class="step hot">Type inference<small>every value</small></div><div class="arrow">→</div>
  <div class="step">C code</div><div class="arrow">→</div>
  <div class="step">C compiler</div><div class="arrow">→</div>
  <div class="step hot">Native binary</div>
</div>

- Reads the **whole program** *before* it runs
- Output runs **without Ruby installed** — just libc/libm + a tiny Spinel runtime (GC etc.)
- Ship **one file**, not a folder of `.rb`

<p class="muted text-sm mt-6">github.com/matz/spinel</p>

<!--
[4:00–4:50]
Spinel 是 Matz 今年 3 月開始寫的 Ruby「AOT 編譯器」。
AOT = Ahead-of-Time，執行「之前」就先編譯好。
流程：讀進整個程式 → 推斷每個值的型別 → 產生 C → 交給 C 編譯器 → 得到原生執行檔。
重點：產出的程式不用裝 Ruby 就能跑，只需要系統的 C 函式庫和 Spinel 的小 runtime（負責 GC 等）。
發佈時就是一個檔案，像 Go 或 Rust 那樣。
-->

---

# Ruby in, C out

<div class="grid grid-cols-2 gap-6 mt-4">
<div>

```ruby
# double.rb
def double(x) = x * 2

puts double(21)
```

</div>
<div>

```c
// generated C (simplified)
sp_int sp_double(sp_int lv_x) {
  return sp_int_mul(lv_x, 2LL);
}
```

</div>
</div>

- Spinel sees `x` is **always an Integer** → plain C integer math
- `puts` becomes `printf` — no VM, no method lookup
- This 2-line program → a **153 KB** standalone executable

<!--
[4:50–5:30]
看個最小例子。左邊是 Ruby，double 方法把 x 乘 2。
Spinel 分析整個程式後發現：x 永遠只會是 Integer。
所以右邊產出的 C 裡，x 就是一個普通的 C 整數，乘法就是 C 的整數運算，
puts 直接變成 printf——沒有 VM、沒有動態方法查找，所以快。
這兩行最後編出來是 153 KB 的獨立執行檔。
（spinel 加 -S 參數可以只輸出 C 程式碼，有興趣可以自己玩。）
-->

---

# CRuby vs Spinel

| | **CRuby** | **Spinel** |
|---|---|---|
| Run on | Any machine **with Ruby** | Same OS + CPU, **no Ruby needed** |
| Ship | `.rb` files | **One program file** |
| Code made at runtime | ✅ `eval`, `method_missing`… | ❌ must see all code at compile time |
| `NoMethodError` | When the line runs | Some caught **at compile time** |
| Gems | Bundler, any gem | `spin` tool; gem works only if Spinel can compile it |

<!--
[5:30–6:10]
整理一下差異。
- 執行：CRuby 要有 Ruby；Spinel 不用，但要在編譯時同一種 OS + CPU 上跑。
- 發佈：一堆 .rb vs 一個執行檔。
- 動態產生程式碼：CRuby 可以，Spinel 不行，因為它必須在編譯時看到全部程式。
- 錯誤：有些呼叫不存在方法的錯誤，Spinel 編譯時就會擋下來——有點像有型別的語言。
- Gem：Spinel 有自己的套件工具 spin，社群也做了 Bundler plugin，但 gem 必須能被 Spinel 編譯才能用。
-->

---

# What Spinel says **no** to

```ruby
code = $stdin.gets
eval(code)                      # ❌ refused: eval of a runtime string

names = ENV["FIELDS"].split(",")
names.each { |n| define_method(n) { } }   # ❌ refused: non-literal name

%i[host port].each { |n| define_method(n) { } }  # ✅ literal names are OK
```

- Also unsupported: `method_missing` dispatch, `TracePoint`, refinements, `binding`…
- Spinel **refuses** code it can't be sure about — at compile time
- 🚂 That's why **Rails can't run on Spinel (yet)** — Rails builds methods at runtime

<!--
[6:10–7:00]
這頁對 Rails 新手特別重要。
Spinel 會「拒絕」它沒把握的程式碼，在編譯時就報錯，不會產出任何東西。
- eval 一段執行時才拿到的字串：拒絕。
- define_method 的名字是從 ENV 讀進來的：拒絕。
- 但如果名字直接寫在程式碼裡，像 %i[host port]：OK。

為什麼 Rails 跑不了？
想想 ActiveRecord：User 的 email、name 這些方法，是 Rails 啟動後讀資料庫 schema 才「動態長出來」的。
這正是 Spinel 在編譯時看不到的東西。
所以 Spinel 不是要取代你的 Rails，它比較適合 CLI 工具、小程式、需要效能的獨立元件。
-->

---
clicks: 1
---

# Two types? Spinel **boxes** it

<div class="grid grid-cols-[1.25fr_1fr] gap-8 items-center">
<div>

```ruby
def double(x) = x * 2

puts double(21)     # 42
puts double("ab")   # "abab"
```

```c
// generated C (simplified)
sp_RbVal sp_double(sp_RbVal lv_x) {
  /* GC frame: SP_GC_ROOT_FRAME,
     SP_GC_ENTRY_RBVAL(lv_x) */
  return sp_poly_mul(lv_x, sp_box_int(2LL));
}
```

</div>
<div v-if="$clicks < 1" class="text-base leading-relaxed">

**① Box** — `x` becomes `sp_RbVal`<br>
<span class="muted">type tag + value, not a plain C int</span>

**② Tell the GC** — `x` may hold a String<br>
<span class="muted">that lives in memory</span>

**③ Dispatch at runtime** — `sp_poly_mul`<br>
<span class="muted">checks the tag: Integer → multiply,<br>String → repeat, Float, Array…</span>

<p class="muted text-sm mt-4">Same for <code>puts</code> → <code>sp_poly_puts</code></p>

<p class="muted text-xs mt-2">▶ next: inside <code>sp_poly_mul</code></p>

</div>
<div v-else class="polymul">

<div class="pm-title">Inside <code>sp_poly_mul(a, b)</code> <small>lib/spinel_rt.h</small></div>

```c
typedef struct {
  int tag;     // SP_TAG_INT / FLT / OBJ …
  int cls_id;  // which class, if an object
  union { sp_int i; sp_float f; void *p; … } v;
} sp_RbVal;    // the "box"
```

<table class="pm-table">
<thead><tr><th>tag of a × b</th><th>what happens</th></tr></thead>
<tbody>
<tr><td>Int / Float × Int / Float</td><td>number fast path ⚡</td></tr>
<tr><td>a user object</td><td>coerce / your own <code>*</code></td></tr>
<tr><td>Complex · Rational · Bignum</td><td>their own multiply</td></tr>
<tr class="hit"><td>String × Integer</td><td>repeat → <code>"abab"</code></td></tr>
<tr><td>Array × Integer</td><td>repeat the array</td></tr>
<tr><td>Array × String</td><td>join</td></tr>
<tr><td>anything else</td><td>TypeError</td></tr>
</tbody>
</table>

<p class="muted text-xs mt-1">Checked top to bottom, at runtime, on every call</p>

</div>
</div>

<!--
[7:00–8:15]
剛剛的 double 只收 Integer。如果我再多呼叫一次 double("ab") 呢？
Ruby 本身沒問題，"ab" * 2 就是 "abab"。Spinel 也編得過，但產出的 C 長得完全不一樣：
① 裝箱：x 不能再是單純的 C 整數，而是 sp_RbVal——一個「型別標籤 + 值」的盒子。
② 通知 GC：因為 x 可能是放在記憶體裡的字串，函式要先把 x 登記給垃圾回收器。
③ 執行時分派：x * 2 變成呼叫 sp_poly_mul，它在執行時看標籤，
   是整數就做乘法、是字串就重複、Float、Array 各走各的。puts 也一樣變成 sp_poly_puts。
其實這就是 CRuby 平常一直在做的事——只是 Spinel 只在「真的需要」的地方才付這個代價。

[click] 那 sp_poly_mul 裡面到底做了什麼？它是 Spinel 自帶的 runtime 函式，定義在 lib/spinel_rt.h。
先看上面的「盒子」sp_RbVal：一個 tag 記型別、一個 cls_id 記是哪個 class、一個 union 放值本身。
sp_poly_mul 拿到兩個盒子後，就照這張表由上往下比對 tag：
- 兩邊都是數字（Integer、Float）最常見，所以放最前面當快速路徑；原始碼註解說這是後來特地移上來的，因為裝箱的算術迴圈裡最常見的就是數字。
- 有一邊是你自己定義的物件，就走 coerce 或你自己寫的 *。
- Complex、Rational、大整數各有自己的乘法。
- String 乘 Integer 就是重複字串——我們的 "ab" * 2 = "abab" 就走這裡。
- Array 乘 Integer 是重複陣列，Array 乘 String 是 join。
- 都不符合就丟 TypeError。
重點：原本一條「加 2」的機器指令，現在變成「呼叫函式 + 一連串 if 比對」，而且每次呼叫都要重新比一次。這就是下一頁會看到的代價。
-->

---
clicks: 5
---

# What does **one String call** do?

<StringCallFlow />

<!--
[8:15–9:15]（按 → 逐步播放，共 6 個狀態）
裝箱的代價有多大？文章做了個實驗：跑 2 億次的迴圈。

先看起點：只有 Integer 的時候，x、double 的回傳值、sum 全部都是 C 的整數 sp_int。
C 編譯器直接把 double inline 掉，x * 2 變成「每次加 2」。文章貼的組合語言顯示，每圈大約 8 條機器指令，沒有任何函式呼叫。

[click] 現在只在迴圈「之後」加一行 double("ab")。注意：這行只會執行一次。

[click] 第一步：同一個 method 的所有呼叫點，型別會合併到同一個參數。
第 5 行傳 Integer、第 8 行傳 String，所以 x 變成「Integer 或 String」，只能裝箱成 sp_RbVal。
x * 2 也不能再是單純加法，要變成 sp_poly_mul，在執行時看標籤再決定怎麼乘。

[click] 第二步：double 可能回傳 Integer，也可能回傳 String，所以它的回傳值也被裝箱。

[click] 第三步：第 5 行 sum += double(i) 接住了一個裝箱的值，所以 sum 也被裝箱，+= 變成 sp_poly_add。
注意 sum 我們根本沒改，它是被「傳染」的。

[click] 最後回到迴圈：每一圈都要付出 2 次執行期函式呼叫 + 型別標籤檢查，乘上 2 億次，整個迴圈慢了約 15 倍。
所以結論不只是「method 只收一種參數」，而是「程式裡每一個存值的位置都保持一種型別」。下一頁整理成幾條規則。
-->

---

# Writing Spinel-friendly Ruby

<div class="grid grid-cols-[1.35fr_1fr] gap-6 items-center text-[0.9rem] leading-snug tight-list">
<div>

1. **Every slot keeps one type** — params, returns, ivars, locals, Array/Hash elements
2. **All call sites merge** into one param slot — no per-call-site copies<br><span class="muted">(except methods that <code>yield</code>: inlined at each call site)</span>
3. **Boxing spreads** — poly param → poly return → poly caller
4. **`nil` is fine** — `Integer?` stays unboxed,<br>but `Integer | String` boxes
5. **Need two types? Split the method** — `double_int` / `double_str`

</div>
<div>

**6. Find the slow path:** `spinel --warn-widen`

```text
warning: parameter `o` of `dist2`
  widened to untyped (boxed poly slow path)
note: passed `pts[0]` is untyped
```

<p class="muted text-sm mt-2"><code>--emit-rbs</code> prints the signatures Spinel inferred</p>

</div>
</div>

<p class="muted text-xs mt-6">Source: github.com/matz/spinel README & docs/emit-types.md (master 6df0724e, Nov 21 2026)</p>

<!--
[9:15–10:00]
把上一頁的教訓整理成寫「Spinel 友善 Ruby」的規則：
1. 每個「位置」都保持一種型別：參數、回傳值、instance variable、區域變數、Array/Hash 的元素。
2. 同一個 method 的所有呼叫點，傳進來的型別會合併到同一個參數。
   Spinel 不會幫每個呼叫點各產生一份專用版本——例外是有 yield 的 method，它會在每個呼叫點被 inline，所以各自專用。
3. 裝箱會傳染：參數變 poly，回傳值跟著 poly，接住它的變數也 poly——就是剛剛的 sum。
4. nil 通常沒關係：Integer?（可能是 nil 的 Integer）不用裝箱，nil 會跟值並排存；真正會裝箱的是 Integer | String 這種不同型別的聯集。
5. 真的需要處理兩種型別？拆成兩個 method，讓每個都各自單一型別。
6. 怎麼知道哪裡被裝箱？編譯時加 --warn-widen，Spinel 會告訴你哪個參數或回傳值被放寬成 untyped，還會一路追到源頭。
   --emit-rbs 則會把它推斷出來的每個 method 簽名印出來，很適合拿來學習。
-->

---

# Pin types with **inline RBS**

<div class="grid grid-cols-[1.1fr_1fr] gap-8 items-center">
<div>

```ruby
class Bag
  attr_reader :count #: Integer

  # @rbs @items: Array[Integer]?

  #: (Array[Integer]) -> void
  def initialize(items)
    @items = items
    @count = items.size
  end
end
```

<p class="muted text-sm">Or external signatures: <code>spinel --rbs sig/</code></p>

</div>
<div class="text-[0.9rem] leading-snug tight-list">

- Same **rbs-inline** syntax (`#:`, `# @rbs`) — on by default
- Just comments → **CRuby ignores them**
- An annotation is an **assertion, not a hint** — it pins the slot
- Visible contradiction → **compile error**
- ⚠️ **Trusted, not verified** — a wrong one can misread memory<br><span class="muted text-sm">(<code>-DSP_RBS_CHECK</code> adds runtime checks)</span>
- Unions still box — annotations **don't make mixed types fast**

</div>
</div>

<p class="muted text-xs mt-4">Source: github.com/matz/spinel docs/inline-rbs.md & rbs-extract.md (master 6df0724e, Nov 21 2026)</p>

<!--
[10:00–10:45]
那 Spinel 有沒有像 CRuby 生態的 RBS 那樣標註型別的方式？有，而且直接用 RBS 語法。
左邊是 Spinel 文件的例子，用 rbs-inline 的寫法：#: 寫 method 簽名、# @rbs 寫 instance variable、attr_reader 後面也能接型別。
預設就會讀；對 CRuby 來說這些只是註解，所以同一份程式碼 CRuby 照樣能跑。
也可以把簽名放在外部 .rbs 檔，用 spinel --rbs 目錄 讀進來，效果一樣。

但跟 Steep 那種型別檢查器的心態不同，要注意：
- 在 Spinel 裡標註是「斷言」不是「提示」：它直接把那個位置的型別釘死，推斷不能推翻它。
- 如果編譯時看得出你寫的跟實際存的矛盾，例如標 Integer 卻存 String，會直接編譯錯誤。
- 但看不出來的錯誤標註，Spinel 是「信任」的——文件裡的例子，把 String 的指標當成 Integer 讀出一串奇怪的數字。
  想要保險，可以用 -DSP_RBS_CHECK 編譯，讓它在執行時檢查型別標籤。
- 最後，RBS 的 union 型別在 Spinel 裡還是裝箱，所以標註不會讓「多型別」變快；
  它的用處是幫推斷不出來的地方釘住單一型別，同時當文件。
-->

---

# How fast?

<div class="stats" style="grid-template-columns: repeat(2, 1fr)">
  <div class="stat"><b>13.9×</b><span>faster than CRuby</span></div>
  <div class="stat"><b>4.5×</b><span>faster than CRuby + YJIT</span></div>
</div>

- Geometric mean on **29 of 88** ruby-bench benchmarks (the ones Spinel can run)
- Mostly **micro-benchmarks** — real apps like Rails don't run yet
- ⚠️ Spinel still has bugs where output differs from CRuby

<p class="muted text-sm mt-4">Snapshot Oct 31, 2026 · Spinel 3e867e30 · CRuby 4.0.7 · source: st0012.dev/spinel</p>

<!--
[10:45–11:15]
速度呢？在 ruby-bench 88 個 benchmark 裡，Spinel 目前能跑 29 個。
這 29 個的幾何平均：比 CRuby 快 13.9 倍，比開了 YJIT 的 CRuby 快 4.5 倍。
但要誠實講：這些多是 micro-benchmark，真實應用（像 Rails）還跑不起來，
而且 Spinel 還有輸出跟 CRuby 不一樣的 bug。所以數字參考就好，別拿去說服老闆換掉 production 😆
-->

---

# Moving *really* fast

<div class="stats">
  <div class="stat"><b>22k+</b><span>commits</span></div>
  <div class="stat"><b>5.6k+</b><span>PRs merged</span></div>
  <div class="stat"><b>100+</b><span>contributors</span></div>
  <div class="stat"><b>10.9k</b><span>test programs</span></div>
</div>

<p class="text-xl mt-10 text-center">All since <span class="mark">Mar 16, 2026</span> — Matz worked solo for the first 5 weeks</p>

<p class="muted text-sm text-center">Each test = a Ruby program whose output must match CRuby</p>

<!--
[11:15–11:40]
最後一個讓人驚訝的數字：發展速度。
從 3 月 16 日 Matz 第一個 commit 到 10 月底：
兩萬兩千多個 commit、合併超過 5,600 個 PR、上百位貢獻者、將近 11,000 個測試程式。
前 5 週是 Matz 一個人寫的，9 月底之後貢獻者暴增。
每個測試都是一支 Ruby 程式，Spinel 的輸出必須跟 CRuby 一模一樣。
這也是一個參與 OSS 的好機會——跟今晚最後的開放討論主題剛好呼應。
-->

---
layout: cover
class: p-0
---

<div class="rt-red-bg flex flex-col items-center justify-center text-center gap-5 px-16">
  <h1 class="!text-white !text-4xl !m-0">TL;DR</h1>
  <ul class="text-xl text-left leading-relaxed">
    <li>Spinel = <b>Ruby → C → native binary</b>, by Matz</li>
    <li>Fast & no Ruby needed — but <b>no runtime magic</b></li>
    <li>Fastest when <b>each value keeps one type</b> — inline RBS can pin it</li>
    <li>Not a Rails replacement — think <b>CLI tools & small programs</b></li>
  </ul>
  <p class="lobster text-3xl mt-4">Up next: Hello, Spinel! — Aotokitsuruya</p>
  <p class="text-sm opacity-80">github.com/matz/spinel · st0012.dev/spinel</p>
</div>

<!--
[11:40–12:10]
總結四句話：
1. Spinel 把 Ruby 編成 C 再變成原生執行檔，作者是 Matz。
2. 很快、不用裝 Ruby，但代價是不能用執行期的動態魔法。
3. 每個值保持一種型別最快，推斷不出來的地方可以用 inline RBS 釘住。
4. 它不是來取代 Rails 的，比較適合 CLI 工具和小程式。
想看它實際能做什麼？接下來交給 Aotokitsuruya，
他會現場 demo 用 Spinel 做語音轉字幕、打包成單一執行檔。掌聲歡迎！
-->
