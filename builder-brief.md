# Builder brief — {{YOUR_BRAND}}

> **Generated from:** https://viktor.com
> **Date:** 2026-06-16
>
> This brief carries the design language of viktor.com, translated for you to apply to **{{YOUR_BRAND}}** — *local AI systems and lead generation for local businesses*.
>
> The source is the inspiration. The brand below is yours. Nothing about your product or copy is copied from the source — only the typographic system, spacing rhythm, and layout patterns.

---

## What makes Viktor feel the way it does

Three invisible choices create the warm-but-technical tone:

**1. The background is warm beige (#faf5f1), not white.**
This is the single biggest reason the site doesn't feel cold or corporate. It reads like cream paper, not a sterile interface. Combined with the peach/orange accent (`#ffbb98`), it evokes warmth and trust — which is exactly what local business owners need to feel before they hand money to an AI company. If you swap this to `#ffffff`, the site immediately reads as generic SaaS. Don't.

**2. All headings use -0.06em letter-spacing.**
That's tighter than almost anything you'll see on a template. Combined with UlmGrotesk Bold (a geometric grotesque), it creates compressed editorial authority — like a broadsheet headline, not a billboard. It signals confidence and specificity. Even if you substitute a free font, preserve this tracking value. It is load-bearing.

**3. Two fonts, two jobs: UlmGrotesk (machine) + Gellix (human).**
UlmGrotesk is geometric and stark — it says "system, precision, AI." Gellix is a humanist sans-serif — it says "readable, approachable, trustworthy." Together they make the split-brain promise of your product: serious automation delivered with human care. If using free fonts, substitute **Space Grotesk Bold** for headings and **Plus Jakarta Sans** for body — they preserve the geometric/humanist contrast.

---

## Tokens — extracted verbatim from viktor.com production CSS

Paste this `:root` block into your CSS. Do not round values.

```css
:root {
  /* Palette */
  --bg-primary:         #faf5f1;
  --bg-secondary:       #fff;
  --bg-contrast:        #1a182b;
  --text-primary:       #1a182b;
  --text-secondary:     #9693a3;
  --text-inverse:       #fff;
  --accent-purple:      #6e47ff;
  --accent-orange:      #ffbb98;
  --deep-blue:          #150079;
  --border-main:        rgba(26, 24, 43, 0.08);
  --border-secondary:   rgba(26, 24, 43, 0.10);

  /* Typography */
  --font-heading:       'UlmGrotesk', 'Space Grotesk', sans-serif;
  --font-body:          'Gellix', 'Plus Jakarta Sans', 'Inter', sans-serif;
  --font-mono:          'Roboto Mono', monospace;

  --h1-size:            3.5rem;
  --h1-leading:         1.1;
  --h1-tracking:        -0.06em;

  --h2-size:            2.75rem;
  --h2-leading:         1.1;
  --h2-tracking:        -0.06em;

  --h3-size:            2.25rem;
  --h3-leading:         1.1;
  --h3-tracking:        -0.06em;

  --h4-size:            1.625rem;
  --h4-leading:         1.1;
  --h4-tracking:        -0.06em;

  --body-large:         1.25rem;
  --body-main:          1rem;
  --body-small:         0.875rem;
  --body-line-height:   1.4;

  /* Spacing */
  --section-py:         120px;
  --container-max:      1200px;
  --container-px:       24px;

  /* Radius */
  --radius-sm:          6px;
  --radius-md:          10px;
  --radius-lg:          16px;
  --radius-xl:          24px;
  --radius-pill:        999px;

  /* Shadows */
  --shadow-card:        0 16px 32px 0 rgba(26, 24, 43, 0.16);
  --shadow-subtle:      0 8px 16px 0 rgba(26, 24, 43, 0.06);

  /* Buttons */
  --btn-border-width:   1.25px;
}
```

---

## The three production moves to preserve

**1. Tight heading tracking (-0.06em on all h1–h4).** Viktor applies this uniformly across every heading level. It's what gives the type its editorial, compressed quality. Do not soften this to -0.02em or -0.03em — the whole feel changes.

**2. Static bold weights, not variable fonts.** Viktor uses static font files (UlmGrotesk-Bold.woff2 at weight 700, Gellix-Regular/Medium at 400/500). No variable font axes in play. The equivalent move in free fonts: set headings to `font-weight: 700` and body to `font-weight: 400`, with `font-weight: 500` for UI labels and eyebrows.

**3. Border-based depth, not box shadows.** Surfaces lift via low-alpha borders (`rgba(26,24,43,0.08–0.14)`) rather than heavy drop shadows. The one exception is the chat card demo, which uses `0 16px 32px 0 rgba(26,24,43,0.16)` — a single restrained shadow. This keeps the warm beige background breathing without making the page feel heavy.

---

## Page structure — 7 sections in this order

*Do not add sections. Do not reorder. Each section is min-height 100vh on desktop.*

### 01 · Nav (sticky)
- Blurred backdrop (`backdrop-filter: blur(12px)`)
- 1px bottom border at `var(--border-main)`
- **Left:** logo mark + brand wordmark
- **Center:** 4–5 nav links, pill hover state at `var(--border-secondary)`
- **Right:** dark pill CTA (e.g. "Book a call")

### 02 · Hero (full viewport, center-aligned)
- Small eyebrow pill: social proof number (e.g. "47 local businesses automated")
- Massive headline using `var(--h1-size)`, `var(--h1-tracking)`, `var(--font-heading)` — with typed-letter animation + blinking cursor in `var(--accent-orange)`
- Lede paragraph: `var(--body-large)`, max 38ch, `var(--text-secondary)` colour
- Two pill CTAs: dark primary ("Book a call") + ghost secondary ("See how it works")
- Below CTAs: small brand logos of trusted local businesses (optionally as a slow scroll ticker)

### 03 · Problem/comparison section
- Eyebrow + h2 on the left: "You've tried the chatbots. Your phones still aren't ringing."
- Two-column comparison: "Other tools" (grey, low contrast) vs. "{{YOUR_BRAND}}" (full contrast, purple accent)
- Per comparison row: plain text task on left, result on right. 4 rows minimum.

### 04 · How it works (3 steps)
- Section eyebrow + h2 centered above
- 3 articles in a row: `/01 Connect`, `/02 You ask`, `/03 It delivers`
- Each article: big section number (`var(--text-secondary)`, mono font), short heading, 2-line body, small chat/UI mockup illustration or screenshot

### 05 · Results carousel (horizontal scroll-snap)
- 5 cards minimum, each 360px wide, `scroll-snap-align: start`
- Per card: local business type badge, result headline (bold number + outcome), 2-sentence story, business name
- Prev/next circular 48px nav buttons at top-right of section

### 06 · Dark CTA band (full-width inverse)
- Background: `var(--bg-contrast)` (`#1a182b`)
- Typed headline with blinking `var(--accent-orange)` cursor
- Subhead: 1 sentence in `var(--text-secondary)` but on dark — adjust to `rgba(255,255,255,0.6)`
- One light pill CTA

### 07 · Footer
- 4-column grid: tagline + 3 link columns
- Giant brand wordmark at centre (line-height 0.85, heading font, full-width)
- Bottom row: small logo + legal links + copyright

---

## House rules

- No drop shadows except on the chat card demo.
- No stock photos. UI screenshots and abstract gradient patches only.
- One accent colour per screen — purple (`#6e47ff`) or orange (`#ffbb98`), not both at once.
- Body line length caps at 60ch — never run full container width.
- Sections ≥120px vertical padding on desktop.
- No scroll-jacking. Native scroll only.
- CTAs ≤4 words.
- **Banned words:** revolutionary, seamless, unleash, empower, transform, game-changing, supercharge, world-class, cutting-edge, next-generation.
- Don't invent sections — exactly the 7 above.

---

## Copy slots — fill these before pasting to v0/Lovable/Claude

```
NAV
  Brand wordmark:        {{YOUR_BRAND}}
  Links:                 How it works, Results, Pricing, FAQ
  CTA:                   Book a call

HERO
  Eyebrow:               {{NUMBER}} local businesses automated
  Headline:              {{HERO_HEADLINE}}  (≤6 words, declarative)
  Lede:                  {{HERO_LEDE}}  (1 sentence, ≤60ch)
  Primary CTA:           Book a call
  Secondary CTA:         See how it works

PROBLEM SECTION
  Eyebrow:               The problem
  Headline:              {{PROBLEM_HEADLINE}}  (≤10 words)
  Row 1 other / yours:   "Chatbots answer questions" / "Your phone rings with booked leads"
  Row 2 other / yours:   "You write the follow-ups" / "Follow-ups go out while you sleep"
  Row 3 other / yours:   "You manage the tool" / "We set it up, maintain it, and report back"
  Row 4 other / yours:   "Monthly SaaS fee forever" / "Done-for-you. Fixed price."

HOW IT WORKS
  Eyebrow:               Simple by design
  Headline:              Up and running in 48 hours.
  Step 1:                Connect — We plug your systems together (CRM, phone, forms)
  Step 2:                Ask — Tell us what a good lead looks like
  Step 3:                Deliver — Your AI system qualifies, follows up, and books calls

RESULTS (5 cards)
  Card 1: [Business type] / [# leads/month or % increase] / [2-sentence story]
  Card 2: …
  Card 3: …
  Card 4: …
  Card 5: …

DARK CTA
  Headline:              {{DL_HEADLINE}}  (5–7 words)
  Subhead:               {{DL_SUBHEAD}}  (1 sentence)
  CTA:                   Book a call

FOOTER
  Tagline:               AI that works for local.
  Wordmark:              {{YOUR_BRAND_UPPERCASE}}
```

---

## Acceptance criteria

A. Every token from the `:root` block above appears verbatim — no rounding.
B. Background is `#faf5f1` on all light sections — no pure white pages.
C. All h1–h4 have `letter-spacing: -0.06em` and `font-weight: 700`.
D. The 7 sections appear in the prescribed order. No extras.
E. At least one scroll-snap carousel functional (results section).
F. Typed-letter animation in hero + dark CTA.
G. Mobile: hero headline ≥40px, columns stack, carousels swipeable.

Return one self-contained HTML file (or Next.js page + global CSS) ready to deploy.

---

*Brief generated by the `design-language` skill — viktor.com → {{YOUR_BRAND}}.*
