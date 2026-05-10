# Design Extract Skill

## Purpose
Given a brand website URL or company name, extracts their design DNA (colors, typography, spacing, voice, component patterns) and outputs a DESIGN.md skeleton ready to adapt for your project.

## How to Use
```
/use design-extract

[Provide either:]
1. A website URL: https://stripe.com or https://notion.so
2. A company name from the awesome-design-md library: "Stripe", "Airbnb", "Linear", etc.
3. Optional: "I need a landing page, focus on hero + CTA components"
```

## What You Get

**Extracted design DNA:**
- Color palette (primary, secondary, accent, how they use them)
- Typography system (scales they use, font families, weights)
- Spacing grid (how they space elements)
- Component patterns (buttons, cards, forms, navigation)
- Visual philosophy (minimal vs bold, light vs dark, etc.)

**Output format:**
A DESIGN.md skeleton you can copy directly into your project and customize.

## Example: Input "Stripe.com"

```
DESIGN EXTRACT: Stripe
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SOURCE: https://stripe.com
CATEGORY: Fintech/Payment
PHILOSOPHY: Clean, minimal, high-trust professional

COLORS
━━━━━━
Primary Background: #ffffff (pure white)
Text Primary: #0a0a0a (near-black)
Text Secondary: #666666 (medium gray)
Accent Primary: #0066ff (bright blue)
Accent Secondary: #635bff (purple — secondary actions)
Neutral Surface: #f6f6f6 (light gray for cards)
Border: #e0e0e0 (subtle dividers)

60-30-10 SPLIT: 60% white bg, 30% gray UI, 10% bright blue CTAs

TYPOGRAPHY
━━━━━━━━━━━
Font: Inter (sans-serif, open source)
Hero Title: 56–64px, 600wt, -0.5px letter-spacing
Section Heading: 36–42px, 600wt
Body: 16px, 400wt, line-height 1.5
Label/Caption: 12–14px, 500wt
All sizes scale down proportionally on mobile

SPACING GRID
━━━━━━━━━━━
xs: 4px | sm: 8px | md: 16px | lg: 24px | xl: 32px | xxl: 48px
Padding: 48px on desktop, 24px on mobile
Gap between sections: 64–80px

COMPONENTS
━━━━━━━━━━
CTA Button: 16px body text, 12px padding vertical, 24px horizontal, 8px border-radius
Card: 16px rounded, 24px padding, 1px border (#e0e0e0)
Form Field: 16px input, 12px padding, border on focus only
Nav: 16px links, blue (#0066ff) on hover/active, no underlines

VOICE & TONE
━━━━━━━━━━━
Confident, clear, action-oriented. No fluff, no decoration. Every word earns its space.

DESIGN PHILOSOPHY
━━━━━━━━━━━━━━━━
- Whitespace = trust (generous padding, breathing room)
- Color = action (only the CTA is bright; everything else is neutral)
- Type = hierarchy (6 sizes max, all derived from base)
- Alignment = structure (16px grid, everything lines up)

YOUR DESIGN.MD STARTING POINT:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━

---
name: My Landing Page (Inspired by Stripe)
description: Clean, minimal fintech aesthetic with bright CTA accent
reference: https://stripe.com

colors:
  background-primary: "#ffffff"
  background-secondary: "#f6f6f6"
  text-primary: "#0a0a0a"
  text-secondary: "#666666"
  text-muted: "#999999"
  accent-primary: "#0066ff"
  accent-secondary: "#635bff"
  border: "#e0e0e0"
  error: "#d32f2f"

typography:
  hero:
    fontFamily: "Inter, sans-serif"
    fontSize: 56px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.5px
  
  heading:
    fontFamily: "Inter, sans-serif"
    fontSize: 36px
    fontWeight: 600
    lineHeight: 1.3
  
  body:
    fontFamily: "Inter, sans-serif"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
  
  label:
    fontFamily: "Inter, sans-serif"
    fontSize: 12px
    fontWeight: 500
    textTransform: uppercase

spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  section-gap: 64px
  padding-desktop: 48px
  padding-mobile: 24px

components:
  button-cta:
    padding: "12px 24px"
    fontSize: "16px"
    fontWeight: 600
    borderRadius: "8px"
    backgroundColor: "#0066ff"
    textColor: "#ffffff"
  
  card:
    padding: "24px"
    borderRadius: "16px"
    border: "1px solid #e0e0e0"
    backgroundColor: "#ffffff"

dos:
  - Use whitespace generously (min 48px padding)
  - CTA is the only bright color (blue); keep UI neutral
  - Keep type to 6 scales max, all derived from 16px base
  - Align everything to 16px grid
  - One clear action per section

donts:
  - Don't use decorative colors (blue is reserved for action)
  - Don't crowd elements (whitespace = professionalism here)
  - Don't mix multiple fonts (Inter only)
  - Don't make forms complex (one field per row on mobile)
  - Don't use motion (static = trustworthy in fintech)

---
```

## Library: 73 Pre-Built Brand Extracts

You have access to 73 already-extracted brand systems in ~/design-systems-reference/design-md/. This skill can pull from them instantly:

**For landing pages:** Stripe, Notion, Linear, Vercel, Slack, Figma
**For trust/premium:** Apple, Nike, Mastercard, BMW
**For bold/expressive:** Spotify, Airbnb, Tesla, PlayStation
**For minimal/data:** GitHub, Wired, IBM

Just name the brand and this skill pulls the pre-built extract.

## When to Use This Skill

- Starting a new project and want inspiration from a proven brand
- Your client says "make it look like Stripe" or "feel like Notion"
- Need a DESIGN.md template but don't want to start from scratch
- Want to compare your color system against what established brands do
- Researching how to structure your nav, CTA placement, form layout

## Integration with Other Skills

- **power-design-audit**: After extraction, audit the extracted palette against Rule 12 (60-30-10)
- **color-system-builder**: If the extracted colors don't fit your brand, use this to rebuild
- **layout-validator**: Use extracted component patterns as your F-pattern reference
- **awesome-design-lookup**: Deep-dive into a specific component (e.g., "how does Notion do card hover states?")

---

**Output is immediately usable** — copy the DESIGN.md skeleton into your project, customize the colors/copy, and ship.
