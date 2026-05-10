# Awesome Design Lookup Skill

## Purpose
Access 73 pre-built brand design systems instantly. Ask how any brand does something, and pull their approach: "How does Stripe design CTAs?", "What's Notion's type scale?", "Show me Airbnb's spacing grid."

## How to Use
```
/use awesome-design-lookup

[Ask about any brand/pattern combination:]
- "How does Stripe structure hero sections?"
- "What's Notion's button styling?"
- "Show me Airbnb's color palette"
- "How does Apple use whitespace?"
- "What fonts does Linear use?"
```

## Available Brands (73 Total)

### Tech / AI / Developer Tools (30)
Anthropic, Claude, OpenAI, DeepSeek, Linear, Vercel, Stripe, Cursor, GitHub, Figma, Webflow, Framer, Mintlify, Notion, Raycast, Lovable, Resend, Sentry, Supabase, Superhuman, MongoDB, Sanity, Posthog, Replicate, Runway, Hashicorp, ElevenLabs, Cal, Clay, Composio, ClickHouse, Cohere, Mistral, Together, x.ai, Ollama, OpenCode, Expo, Pinterest

### Finance / Payment (6)
Stripe, Mastercard, Coinbase, Binance, Kraken, Revolut, Wise, Shopify

### Auto / Lifestyle (6)
Tesla, BMW, BMW M, Bugatti, Ferrari, Lamborghini, Renault, Nike, Airbnb, Apple, Starbucks, Grind, Vodafone

### Media / Entertainment (5)
The Verge, Wired, Spotify, YouTube, Sony, PlayStation, IBM

### Productivity / Operations (5)
Notion, Slack, Miro, Intercom, Zapier, Uber, NVIDIA, SpaceX, VoltAgent, Warp

## Example Lookups

### Query: "How does Stripe design CTAs?"

```
STRIPE CTA DESIGN
━━━━━━━━━━━━━━━━━

Brand Context: Fintech/Payment processor, trust-focused

CTA Button Anatomy:
  Color: Bright blue (#0066ff) — single accent color on white
  Padding: 12–16px vertical × 24–32px horizontal
  Typography: 16px, 600wt (bold, readable)
  Border Radius: 8px (slightly rounded, not pill-shaped)
  Hover State: Slight darken + cursor pointer
  Shadow: None (flatness = modernity here)
  
Text Variants:
  Primary Action: "Get Started" or "Create Account" (action verb)
  Secondary: Uses lighter color or outline style
  Disabled: Grayed out (50% opacity)

Placement:
  Hero CTA: End of headline, slightly offset right
  Mid-page CTA: Centered below content section
  Multiple CTAs: Primary (blue) + Secondary (outline) stacked vertically
  
Why This Works for Stripe:
  - Blue is reserved (not used elsewhere), so CTA stands out
  - Bold typography (600wt) signals "tap me"
  - Generous padding makes touch target large (mobile-friendly)
  - Rounded corners feel modern, not corporate
  
YOUR ADAPTATION:
  If you're using Stripe's approach:
  ✅ Keep one accent color (yours: #cc8832 or #3b5e3a)
  ✅ Make it 16px, 600wt
  ✅ Padding: 12–16px × 24px minimum
  ✅ Rounded: 8px
  ✅ Hover: Darken 20%

COMPARE: How does this differ from Notion?
  Notion uses softer, more rounded buttons (12px radius)
  Notion often uses muted accent (not bright blue)
  Stripe is bolder + higher contrast
  → Notion for tech/creative, Stripe for finance/trust
```

### Query: "What's Notion's type scale?"

```
NOTION TYPOGRAPHY
━━━━━━━━━━━━━━━━

Font Family: Inter (sans-serif, same as Stripe)
Philosophy: Clean, readable, generous line-height

Scale (in pixels):
  Display XL:  56px, 700wt, line-height 1.2   (main hero headlines)
  Display LG:  42px, 700wt, line-height 1.2   (section headers)
  Display SM:  32px, 700wt, line-height 1.3   (subsections)
  Body LG:     20px, 400wt, line-height 1.6   (body text, readable)
  Body:        16px, 400wt, line-height 1.6   (default, dense)
  Label:       12px, 600wt, line-height 1.4   (captions, buttons)

Letter Spacing:
  Headlines: -0.3px to -0.5px (tight, modern)
  Body: 0 to 0.2px (normal, readable)

Line Height Philosophy:
  Headlines: 1.1–1.3 (tight, drama)
  Body: 1.5–1.6 (generous, readability)
  Forms: 1.4 (slightly tight, functional)

Why This Works:
  - Limited scales (5) creates consistency
  - Generous body line-height (1.6) = effortless reading
  - Letter spacing on headlines gives modernity
  - Everything scales proportionally on mobile

YOUR ADAPTATION:
  If adopting Notion's approach:
  ✅ Limit to 5–6 type scales max
  ✅ Use Inter or similar humanist sans-serif
  ✅ Body line-height ≥1.5 (not 1.4)
  ✅ Tighten headlines with -0.3 to -0.5px letter-spacing
  ✅ Reduce letter-spacing on body (let it breathe naturally)
```

### Query: "Show me Apple's color philosophy"

```
APPLE COLOR STRATEGY
━━━━━━━━━━━━━━━━━━━

Primary Palette:
  White: #ffffff (dominant, ~80% of page)
  Black: #1d1d1d (text, emphasis)
  Gray: #f5f5f5, #e0e0e0, #999 (layering, hierarchy)
  Accent: Subtle, context-dependent (gold, silver, rarely bold colors)

60-30-10 Split:
  60% = Pure white background
  30% = Gray surfaces, white text on dark, subtle borders
  10% = Minimal accent (usually product color, not bright)

Design Philosophy:
  "Color is restraint. Whitespace speaks louder than saturation."
  
  Consequences:
    ✓ Feels premium, not chaotic
    ✓ Product image dominates (no competing colors)
    ✓ Text reads effortlessly (high contrast)
    ✗ Takes discipline (can't use color as crutch)

When Apple Uses Color:
  - Product hero (iPhone, Mac photos — the product IS the color)
  - Accent (usually the product itself, not arbitrary UI)
  - Never for hierarchy (they use whitespace + size instead)

YOUR ADAPTATION:
  If adopting Apple's restraint:
  ✅ Use white/light backgrounds (80%+)
  ✅ Keep text black or near-black (high contrast)
  ✅ Limit accent to one color (your product, your brand)
  ✅ Use spacing + size for hierarchy, not color
  ✅ Test with all images removed — does layout still work? (If yes, design is solid)

COMPARE: How does Apple differ from Spotify?
  Spotify uses bold, saturated colors (green, black, accent colors)
  Apple uses white + black + minimal accent
  → Spotify for energy/music, Apple for premium/restraint
```

## Library Structure

Your 73 brands are stored in: `~/design-systems-reference/design-md/[brand-name]/brand-style.md`

Each file contains:
- Brand philosophy (why they design the way they do)
- Color palette (hex + usage)
- Typography (scales, font families, weights)
- Component patterns (buttons, cards, forms, navigation)
- Spacing grid (how they space elements)
- When to use this brand as reference
- Voice & tone notes

You can also browse all 73 at: `~/design-systems-reference/README.md`

## Query Types Supported

**Single Brand:**
- "How does Stripe design CTAs?" → pulls Stripe's button approach
- "What's Notion's color palette?" → pulls exact hex values + usage

**Brand Comparison:**
- "How do Stripe and Notion differ?" → side-by-side analysis
- "Which brand uses bold colors?" → searches across all 73 for similar approaches
- "Show me premium brands' typography" → pulls Apple, Nike, Tesla patterns

**Pattern Across Brands:**
- "How do 5 tech brands space their components?" → searches for spacing philosophy
- "Which brands use serif fonts?" → searches across the library
- "What's the most common button styling?" → aggregate findings

**Industry-Specific:**
- "Show me fintech design" → Stripe, Coinbase, Wise, Mastercard patterns
- "How do tech SaaS companies do hero sections?" → Linear, Vercel, Figma, Notion approaches
- "What's the pattern for ecommerce?" → Shopify, Airbnb, Nike analysis

## When to Use This Skill

- You want to reference how a proven brand solves a problem
- Your client says "make it feel like Stripe/Notion/Apple"
- You're stuck on a design decision (color, typography, spacing)
- Researching a specific brand for inspiration
- Comparing your approach against industry standards
- Building a component (button, card, form) and want reference

## Integration with Other Skills

- **design-extract**: Use this as the source for brand extraction
- **power-design-audit**: Cross-check if famous brands follow the 10 rules (spoiler: they do)
- **color-system-builder**: See how brands build 60-30-10 palettes
- **layout-validator**: Compare your F-pattern against how brands layout content

---

**No guessing required** — all 73 brands are documented and searchable. Ask specifically, get specific answers.
