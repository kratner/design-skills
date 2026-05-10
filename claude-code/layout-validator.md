# Layout Validator Skill

## Purpose
Checks your landing page layout against three foundational design principles: F-pattern eye flow, 8pt grid alignment, and whitespace ratio. Identifies structural issues before you build.

## How to Use
```
/use layout-validator

[Describe your layout:]
1. What sections do you have? (hero, feature grid, testimonials, CTA, etc.)
2. What's in each section? (headline, image, form, button, etc.)
3. Rough sizing: is the hero taking up 40% of page or 20%?
4. What's the viewport? (mobile, desktop, or both?)
```

## Three Core Validations

### 1. F-Pattern Eye Flow

Users scan web pages in an F:
- Horizontal line across top (headline, nav)
- Vertical line down left side (first item, navigation)
- Horizontal line across middle (secondary content)

**Valid F-pattern:**
```
┌──────────────────────────────────────┐
│ HEADLINE                             │  ← Horizontal scan (top)
├─┐                                    │
│ │ Image or key visual (left)         │
│ │                                    │
│ └─→ Supporting text (flows right)    │
│                                      │
│ SECONDARY HEADING                    │  ← Horizontal scan (middle)
│                                      │
│ Feature 1    Feature 2    Feature 3  │
│                                      │
│              [CTA Button]            │  ← CTA natural endpoint
└──────────────────────────────────────┘
```

**Invalid (broken F-pattern):**
- Centered everything (no left-edge anchor)
- Key visual on right instead of left
- CTA before content (unnatural flow)
- Multiple competing focal points (user doesn't know where to look)

### 2. 8pt Grid Alignment

All spacing must align to 8pt multiples: 8, 16, 24, 32, 48, 64, 80, 96px.

**Valid:** Padding 24px, gap 16px, margin 48px
**Invalid:** Padding 23px, gap 15px, margin 37px

Why? Consistency. Everything feels intentional, not random.

### 3. Whitespace Ratio

Minimum 40% of bounding box must be empty space. Too dense = chaotic.

**Valid:** Hero section with headline, image, CTA = 50% whitespace
**Invalid:** Hero packed with headline, 3 images, nav, form = 15% whitespace

## Example Validation

```
LAYOUT VALIDATOR: Opt-In Landing Page
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

INPUT LAYOUT:
- Hero: "Get AI Workflows Free" headline, background image, email form, CTA
- Social Proof: 3 testimonial cards
- FAQ: 5 accordion sections
- Footer: Links, copyright

VALIDATION 1: F-PATTERN
━━━━━━━━━━━━━━━━━━━━━━━
Hero Analysis:
  Headline: Left-aligned ✅
  Image: Full-width background ⚠️ (blocks left-edge navigation)
  Form: Center-aligned ⚠️ (breaks F-pattern flow)
  CTA: Under form ✅

Verdict: PARTIAL ⚠️
- Headline anchors left (good)
- Background image is immersive but blocks natural left-edge scan
- Centered form is OK for opt-ins (user expects center), but place CTA slightly left for better flow

FIX: Move email form 10–15% left from center, keep CTA directly below (not offset)

Social Proof Analysis:
  Cards: 3 columns, evenly spaced ✅
  Text: Left-aligned within cards ✅
  
Verdict: PASS ✅

8PT GRID ALIGNMENT
━━━━━━━━━━━━━━━━━
Current Spacing Audit:
  Hero padding: 40px ❌ (should be 48px or 32px)
  Card gap: 20px ❌ (should be 24px or 16px)
  Form field margins: 12px ❌ (should be 16px or 8px)
  Footer padding: 48px ✅

Verdict: FAIL ⚠️
- 3 of 4 spacing values are off-grid
- Easy fix: Update hero padding to 48px, gaps to 24px, form margins to 16px

FIX COMMANDS:
  hero { padding: 48px; }
  .card { gap: 24px; }
  .form-field { margin: 16px 0; }

WHITESPACE RATIO
━━━━━━━━━━━━━━━
Section Analysis:
  Hero (1920×800px = 1,536,000px²)
    - Content (headline, form, CTA): ~400,000px²
    - Whitespace: ~1,136,000px² = 74% ✅ (exceeds 40%)
  
  Social Proof (1920×400px = 768,000px²)
    - Content (3 cards + text): ~500,000px²
    - Whitespace: ~268,000px² = 35% ❌ (below 40%)
  
  FAQ (1920×600px = 1,152,000px²)
    - Content (5 accordions): ~700,000px²
    - Whitespace: ~452,000px² = 39% ❌ (just below 40%)

Verdict: PARTIAL ⚠️
- Hero is spacious (good)
- Social Proof section is too dense
- FAQ section is borderline

FIXES:
  - Add 24–32px padding to social proof container
  - Increase gap between cards from 16px to 24px
  - Add 16–24px top margin to FAQ section
  - These will push whitespace to 42–45% ✅

OVERALL SCORE: 6.5/10
━━━━━━━━━━━━━━━━━━━━━━
✅ F-Pattern: 6/10 (hero flows, but centered form breaks natural scan)
⚠️  8pt Grid: 3/10 (multiple spacing values off-grid)
⚠️  Whitespace: 7/10 (hero good, social proof + FAQ too dense)

PRIORITY FIXES (in order):
1. Fix 8pt grid spacing (fastest, immediate impact)
   → Hero padding: 40px → 48px
   → Card gap: 20px → 24px
   → Form margins: 12px → 16px
   
2. Add whitespace to social proof section
   → Add container padding 32px
   → Increase card gap from 16px to 24px
   
3. Adjust form position for better F-pattern flow
   → Shift form 10–15% left from center (feels more natural in flow)

AFTER FIXES: Expect 8.5/10 score ✅
```

## Validation Checklist

When you describe your layout, this skill checks:

**F-Pattern Questions:**
- [ ] Is your hero headline on the left?
- [ ] Is your key visual on the left (or full-width)?
- [ ] Do secondary elements flow naturally from left to right?
- [ ] Is your CTA at a natural reading endpoint?
- [ ] Is there one clear focal point per section (not 3+)?

**8pt Grid Questions:**
- [ ] Are all padding/margins 8, 16, 24, 32, 48, 64, etc.?
- [ ] Are element gaps consistent (not random)?
- [ ] Do all edges align to a common vertical grid?

**Whitespace Questions:**
- [ ] Does each section have ≥40% empty space?
- [ ] Can the eye rest, or does the page feel claustrophobic?
- [ ] Is there enough room between sections?

## When to Use This Skill

- You've roughed out a layout but want feedback before building
- A section feels off, but you can't name why
- You're moving from desktop to mobile design
- Before finalizing a design
- As a final check before handing off to a developer

## Integration with Other Skills

- **power-design-audit**: Use this for Rules 15 (8pt grid), 16 (alignment), 4 (whitespace)
- **design-extract**: Compare your layout structure to how Stripe, Notion, etc. arrange content
- **color-system-builder**: Once layout is validated, add colors with confidence

---

**Output includes specific fixes** — pixel values you can implement immediately in your design tool or CSS.
