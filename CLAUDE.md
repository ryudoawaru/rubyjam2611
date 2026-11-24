# CLAUDE.md

Opening talk deck for Ruby Jam, Nov 24 2026 (Ruby Taiwan monthly meetup): "What's Spinel?" — a primer on Matz's Ruby AOT compiler for Rails beginners, given by the organizer before Aotokitsuruya's "Hello, Spinel" talk. Pages 1–7 are the meetup opening (Ruby Jam cover, schedule, sponsors, RubyWorld Conference / Ruby Prize / Ruby biz Grand prix promo, next Ruby Jam); the Spinel talk starts at page 8. Slides are **English**; speaker notes are **Traditional Chinese (Taiwan)**.

## Commands

```bash
yarn dev      # dev server; press `p` for presenter mode (notes + click markers)
yarn build    # build to dist/
yarn export   # PDF export (needs playwright-chromium, already a devDependency)
npx slidev export --format png --with-clicks --range 14 --output <dir>   # check one slide, every click state
```

Always export the changed slide to PNG and look at it after editing — overflow and wrapping only show up rendered.

## Files

- `slides.md` — all content (20 slides). Speaker notes are the `<!-- -->` block at the end of each slide.
- `styles/index.css` — Ruby Taiwan theme + per-slide classes (`.pipe`, `.flow3`, `.stats`, `.polymul`, `.pm-table`, `.tight-list`).
- `components/StringCallFlow.vue` — page 15 click animation (6 states, driven by `useSlideContext().$clicks`).
- `public/` — Ruby Taiwan logo, logotype, geometric background (copied from `~/RubyPrjs/rubytw`).
  Sponsor logos `logo_piccollage.png`, `logo_day1.svg`, `logo_5xruby.svg` (page 3).
  RWC 2026 page 4: `rwc_hero.svg` (final frame of the animated hero SVG on 2026.rubyworld-conf.org/ja/, captured from the live DOM), `rwc_irina.jpg` / `rwc_matz.jpg` (keynote avatars from the same site).
  Page 5: `rwc_ruby_prize.jpg` (banner from the same site).
  QR codes (`qrencode -t SVG -m 2`): `qr_rubyprize.svg` (page 5, rubyprize.jp), `qr_rubybiz.svg` (page 6, rubybiz.jp/#finalist).
  Page 7: `rubyjam_1217_dj.jpg` (DJ Steven photo from the organizer), `qr_rubyjam_1217.svg` = `qrencode -t SVG -m 2` of the Day1 registration URL for the Dec 17 Ruby Jam (event copy from the organizers' Notion page).
  `rb/`: Ruby Prize final-nominee photos (rubyprize.jp); `finalist.png` = 2x Playwright screenshot of rubybiz.jp `#finalist` (page 6, SOSI outline is a %-positioned overlay — re-measure if the screenshot changes).

## Design system (from rubytw `_sass/base/_styleguide.sass`)

- Colors as CSS vars: `--rt-red #bd3f32` (headings, accents), `--rt-yellow #fff59d` (`.mark` highlight), `--rt-deep #323232` (body), `--rt-grey #9b9b9b` (`.muted`).
- Fonts: Montserrat (body/headings), Lobster (`.lobster`, script accents), Fira Code (code). Loaded via `@import` in CSS; headmatter uses `fonts.provider: none`.
- Cover and closing slides: `layout: cover` + `class: p-0` + a `.rt-red-bg` div. Content slides are vertically centered (`.slidev-layout.default` is flex-centered).
- Utility classes: `.red`, `.mark`, `.muted`. Slidev's UnoCSS utilities (`grid-cols-[…]`, `text-[0.9rem]`) work inline.

## Speaker-note conventions

- Each note starts with a time mark like `[5:00–6:15]`. Adding or lengthening a slide means shifting every later mark and `duration:` in the headmatter.
- Click-driven slides: set `clicks: N` in the slide frontmatter, and put one `[click]` marker per click in the notes (text before the first marker is click 0). The count of markers must equal N.

## Click animations

- Swap content on a click with `v-if="$clicks < 1"` / `v-else` plus `clicks: 1` (page 14).
- Reveal in order with plain `v-click` divs (page 9).
- Complex state (page 15) lives in a component that reads `$clicks` from `useSlideContext()` (from `@slidev/client`, Slidev 0.49).

## Content accuracy

Every technical claim must be traceable; don't write Spinel/CRuby internals from memory.

- Primary source: Stan Lo's article https://st0012.dev/spinel/ (snapshot Oct 31 2026, Spinel 3e867e30, CRuby 4.0.7).
- Spinel repo facts (inline RBS, `--warn-widen`, `sp_poly_mul` in `lib/spinel_rt.h`, `sp_RbVal` in `lib/sp_gc.h`) were checked at matz/spinel master `6df0724e` (Nov 21 2026). Spinel moves fast; re-check before the talk. Source lines on slides cite the doc and commit.
- CRuby facts: bytecode is real `ruby --dump=insns` output from local Ruby 4.0.7; `vm_opt_mult` matches `vm_insnhelper.c` at revision `229531a6cf`.
- Generated-C snippets are labeled "(simplified)": only the signature and `return` lines are verbatim.

## Gotchas

- `sed` on this machine is GNU sed: `sed -i 's/…/…/'`, not `sed -i ''`.
  In the replacement, `&` means "the whole match" — slides use `&amp;`, so edit those lines with Python or escape it as `\&`.
- Slidev's default theme fades a `<p>` right after an `h1` (`h1 + p` opacity); add `!opacity-100` when that paragraph should stay solid (page 1 date).
- Raw `<table>` HTML in slides needs explicit `<thead>`/`<tbody>`, otherwise Vue warns.
- The goto-dialog suggestion list is hidden on purpose (`#slidev-goto-dialog .autocomplete-list`); `g` + page number + Enter still works.
