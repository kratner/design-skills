# Color System Builder Skill

## Purpose
Given your hero/primary brand color (one hex value), generates a complete, balanced 60-30-10 color system with contrast validation. Returns a WCAG-compliant palette ready to use immediately.

## How to Use
```
/use color-system-builder

[Provide one of the following:]
1. Your brand's primary/hero color (hex: #cc8832, RGB: 204,136,50, or just "ochre")
2. OR describe what you want: "I want warm and professional" or "tech/modern/cool"
3. Optionally: what's your background? (light, dark, or specific color)
```

## What You Get

**Full color system:**
- Primary background (60%) — where your content lives
- Secondary accents (30%) — supporting UI, borders, subtle elements
- Hero accent (10%) — CTA buttons, highlights, micro-interactions

**Contrast validation:**
- Text on background: ✅ WCAG AA (4.5:1) or ✅ WCAG AAA (7:1)
- Button on background: confirmed readable
- All combinations tested

**Bonus:**
- Opacity variants (50%, 70%, 100% for overlays)
- Hover states (darkened/lightened for interactive elements)
- Grayscale fallback (if color can't be used)

## 60-30-10 Framework

The system uses the classic design principle:
- **60%** = Dominant (usually background + primary text)
- **30%** = Secondary (supporting structure, borders, captions)
- **10%** = Accent (CTA, highlights, emphasis)

This creates balance without chaos. Every color has a role.

## Example: Input "Forest Green" (#3b5e3a)

```
INPUT: Primary Color #3b5e3a (forest green)
Background: Light (assumed for web landing pages)

OUTPUT: COMPLETE COLOR SYSTEM
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

60% DOMINANT (Background & Primary)
├─ Background: #f5f0e0 (cream — high contrast with forest)
├─ Text Primary: #1a1a1a (near-black — 14:1 contrast on cream)
└─ Text Secondary: #666666 (medium gray)

30% SECONDARY (Structure, Borders, Support)
├─ Border: rgba(58,94,58, 0.2) (forest at 20% opacity)
├─ Divider: #e0e0e0 (light gray)
├─ Muted Text: #999999 (lighter gray for captions)
└─ Overlay: rgba(255,255,255, 0.05) (subtle white overlay)

10% ACCENT (CTA, Highlights, Emphasis)
├─ Primary CTA: #3b5e3a (forest green — your input)
├─ CTA Hover: #2d4628 (darkened 20%)
├─ Secondary Accent: #cc8832 (warm ochre — complements forest)
└─ Alert/Error: #c64545 (warm red for warnings)

CONTRAST VALIDATION
━━━━━━━━━━━━━━━━━━
✅ #1a1a1a text on #f5f0e0 bg = 14:1 (WCAG AAA)
✅ #666666 text on #f5f0e0 bg = 8.2:1 (WCAG AAA)
✅ #3b5e3a CTA on #f5f0e0 bg = 4.6:1 (WCAG AA)
✅ #3b5e3a CTA on #ffffff bg = 4.5:1 (WCAG AA, borderline)
✅ White text (#fff) on #3b5e3a = 5.1:1 (WCAG AA)

ALL COMBINATIONS PASS ✅

OPACITY VARIANTS (for depth, layering)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Overlay Light: rgba(255,255,255, 0.05) — subtle layers
Overlay Strong: rgba(255,255,255, 0.15) — visible but translucent
Forest @ 20%: rgba(58,94,58, 0.2) — borders, subtle accents
Forest @ 50%: rgba(58,94,58, 0.5) — semi-transparent panels

QUICK CSS SETUP:
```css
:root {
  --color-bg-primary: #f5f0e0;
  --color-text-primary: #1a1a1a;
  --color-text-secondary: #666666;
  --color-text-muted: #999999;
  --color-accent-primary: #3b5e3a;
  --color-accent-secondary: #cc8832;
  --color-border: rgba(58,94,58, 0.2);
  --color-error: #c64545;
}
```

READY TO USE ✅
```

## Advanced Options

If you want more control, you can specify:
- **Temperature**: cool (blues), warm (reds/oranges), neutral
- **Mood**: professional (muted), playful (bright), minimal (reduced palette)
- **Background**: light/dark/medium
- **Industry hints**: tech (clean blues), fashion (bold), finance (trust colors)

## When to Use This Skill

- Starting a new ClickFunnels page and need palette fast
- Have a brand color but need full system (backgrounds, borders, text)
- Need WCAG contrast validation before building
- Want opacity variants for layering effects
- Building a DESIGN.md and need the colors section filled in

## Integration with Other Skills

- **power-design-audit**: Use this output as your "Rule 12: 60-30-10 Color Split" reference
- **awesome-design-lookup**: Compare your palette against how Stripe, Notion, Airbnb structure theirs
- **layout-validator**: Use these colors in your layout descriptions for better feedback

---

**Output is copy-paste ready** — take the hex values directly into ClickFunnels, Figma, CSS, or your design tool.
