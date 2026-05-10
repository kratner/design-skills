# Power Design Audit Skill

## Purpose
Validates a landing page, section, or design against the 10 critical Power Design principles that matter most for web/landing page conversion. Returns a scorecard with pass/fail on each rule and actionable fixes.

## How to Use
```
/use power-design-audit

[Describe your landing page or design section. Include:]
- What's the page goal? (opt-in, product sale, brand awareness, etc.)
- What's currently on it? (headline, visuals, form fields, CTA, etc.)
- What's your layout? (hero + form, feature grid, testimonials, etc.)
- Any color/text sizing decisions you've made?
```

## Reference: 10 Critical Rules for Landing Pages

| Rule | Criteria | Pass = | Fail = |
|------|----------|--------|--------|
| **Rule 1: One Idea Per Section** | Each section has one clear purpose, not 3+ ideas competing | "This section is about sign-ups. Period." | Headline about features, subtext about pricing, CTA for demo |
| **Rule 2: Glanceable in ≤3 Seconds** | Headline + visual + CTA immediately obvious | User understands purpose before reading body text | User has to read 3+ sentences to understand what page does |
| **Rule 3: ≤7±2 Chunks Per Section** | Max 7 visual groupings (ideal: 3–5) | Hero: headline, image, CTA = 3 chunks | Hero: headline, subheader, 2 images, 2 logos, CTA, form = 6 chunks (borderline) |
| **Rule 4: ≥40% Whitespace** | Empty space ≥ 40% of bounding box | 1 hero section: 40–50% padding/gaps | Dense grid, 20% whitespace, text blocks touching edges |
| **Rule 8: Body ≥24px, Headlines ≥48px** | Readability at mobile + tablet | Body copy 24px+, headlines 48–120px | Body copy 14px, headlines 32px (struggle to read on phone) |
| **Rule 12: 60-30-10 Color Split** | Dominant color 60%, secondary 30%, accent 10% | Background 60%, supporting UI 30%, CTA 10% | Rainbow of equal-weight colors, no visual hierarchy |
| **Rule 15: 8pt Grid** | All spacing in multiples of 8 (16, 24, 32, 48, 64) | Padding 32px, gaps 24px, margins 48px | Padding 23px, gaps 15px, margins 37px (arbitrary) |
| **Rule 16: Align Everything to One Grid** | All edges (text, boxes, images) align to same vertical/horizontal lines | Left edge of headline, form, image all flush | Headline at 40px, form at 45px, image at 50px |
| **Rule 19: F-Pattern Layout** | User's eye naturally flows down left side, then across | Headline (top-left) → body (left edge) → CTA (bottom-right) | Centered layout, multiple focal points, no clear flow |
| **Rule 20: One Mode** | Either Reynolds (big, emotional, movement) OR Tufte (minimal, data-dense) — not both | Big hero image + short copy + bold CTA | Tiny hero image + 500 words of body text + underplayed CTA |

## What You'll Get

The audit returns:
- **Pass/Fail on each of the 10 rules**
- **Specific fixes** (e.g., "Rule 4: Add 20px padding to hero section" or "Rule 12: Your accent should be 10–15% of the page, currently 25%")
- **Priority fixes** (which rules to fix first for max impact)
- **Confidence score** (what % of the rules pass)

## Example Output

```
POWER DESIGN AUDIT: ClickFunnels Opt-In Page

SCORECARD:
✅ Rule 1: One Idea (sign-up focus) — PASS
✅ Rule 2: Glanceable (headline + form obvious) — PASS
⚠️  Rule 3: Visual Chunks (8 chunks, ideal ≤7) — BORDERLINE
❌ Rule 4: Whitespace (22% whitespace, need ≥40%) — FAIL
✅ Rule 8: Type Sizes (headline 60px, body 24px) — PASS
❌ Rule 12: Color Split (60% bg, 20% secondary, 20% accent) — FAIL (accent too prominent)
⚠️  Rule 15: 8pt Grid (mostly 8pt, but margins are 23px) — BORDERLINE
✅ Rule 16: Alignment (all edges flush left) — PASS
✅ Rule 19: F-Pattern (headline top-left, CTA bottom-right) — PASS
✅ Rule 20: One Mode (Reynolds: big hero, short copy) — PASS

OVERALL: 7/10 PASS (70%)

PRIORITY FIXES:
1. Add 40px padding/margins instead of 20px (Rules 4, 15)
2. Reduce accent color usage: move from 20% to 10% (Rule 12)
3. Condense feature section from 8 chunks to 5 (Rule 3)
```

## Notes

- Audit is conversational. Ask follow-up questions if needed.
- Rules are evidence-based (Tufte, Reynolds, Duarte, WCAG, Nielsen Norman Group).
- "Pass" doesn't mean done. Even 10/10 can be better. This is a floor, not a ceiling.
- Use alongside `color-system-builder` and `layout-validator` for complete design check.

---

**When to use this skill:**
- Before finalizing any landing page layout
- When a design "feels off" but you can't name why
- Before handing off to team or client
- As validation for A/B testing (test against the 10 rules)
