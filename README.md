# Design Skills

Portable, evidence-based design tools and frameworks. Use in your personal projects or share selectively with your team. Extensible across platforms (Claude Code skills, web tools, Figma plugins, team documentation).

## Quick Start

```bash
# Clone the repo
git clone https://github.com/kratner/design-skills ~/design-skills

# For Claude Code skills:
git clone https://github.com/kratner/design-skills ~/.claude/skills/design-skills

# In Claude Code, invoke any skill
/use power-design-audit
/use color-system-builder
/use design-extract
/use layout-validator
/use awesome-design-lookup
```

## Current Skills

### 1. **power-design-audit**
Validates any landing page or design section against 10 critical design principles from Power Design. Returns a scorecard (pass/fail on each rule) + actionable fixes.

**Use when:**
- Before finalizing a layout
- Design feels off but you can't name why
- Need validation against evidence-based principles
- Preparing to hand off to team or client

**Example:** `/use power-design-audit` → Describe your hero section → Get 7/10 score with specific fixes

---

### 2. **color-system-builder**
Given one hex color (your brand primary), generates a complete WCAG-compliant 60-30-10 color system. Returns full palette with contrast validation, opacity variants, and CSS variables.

**Use when:**
- Starting a new project with a brand color
- Building DESIGN.md and need the colors section
- Need WCAG AA/AAA contrast verified
- Want opacity variants for layering

**Example:** `/use color-system-builder` → Input `#3b5e3a` → Get full system with hover states and contrast checks

---

### 3. **design-extract**
Given a brand URL (e.g., stripe.com) or company name, extracts their design DNA: colors, typography, spacing, components, philosophy. Outputs a DESIGN.md skeleton ready to customize.

**Use when:**
- Client wants you to "match the Stripe aesthetic"
- Starting a new project and want design inspiration
- Need a DESIGN.md template but want to base it on real brands
- Researching how established brands solve a problem

**Example:** `/use design-extract` → Input "Stripe.com" → Get color palette, type scales, spacing grid, component patterns

---

### 4. **layout-validator**
Checks your layout against three foundational principles: F-pattern eye flow, 8pt grid alignment, and ≥40% whitespace. Identifies structural issues before you build.

**Use when:**
- You've roughed out a layout but want feedback
- Moving from desktop to mobile design
- A section feels dense or chaotic
- Before finalizing in ClickFunnels or Figma

**Example:** `/use layout-validator` → Describe your sections → Get feedback on F-pattern flow, spacing alignment, and whitespace ratio

---

### 5. **awesome-design-lookup**
Access 73 pre-built brand design systems instantly. Ask how any brand does something: "How does Notion style buttons?", "What's Apple's color philosophy?", "Show me Stripe's CTA approach."

**Use when:**
- Researching a specific brand's approach
- Comparing design philosophies across brands
- Building a component and want reference
- Client references a brand you want to learn from

**Example:** `/use awesome-design-lookup` → Ask "How does Stripe design CTAs?" → Get button anatomy, placement, hover states, and how to adapt it

---

## Who This Is For

**Personal Design Work:** ClickFunnels landing pages, demo reels, client projects, branding work. Full access to all skills.

**Team Collaboration:** Optional. Share selectively — decide which skills to introduce, when, and how.

**Design System Building:** Use these skills to generate DESIGN.md templates and validate projects against evidence-based principles.

## Installation

### For Personal Use

```bash
# One-time setup
git clone https://github.com/kratner/design-skills ~/.claude/skills/design-skills

# Update anytime
cd ~/.claude/skills/design-skills && git pull
```

Then in Claude Code:
```
/use power-design-audit
/use color-system-builder
/use design-extract
/use layout-validator
/use awesome-design-lookup
```

### For Team Sharing (Optional)

See `TEAM_SHARING.md` for how to:
- Share individual skills without enforcing them
- Create team documentation from skill definitions
- Set expectations around design principles
- Track which skills the team adopts

---

## How These Skills Connect

```
START A PROJECT
       ↓
design-extract ← Pick a brand for inspiration
       ↓
color-system-builder ← Build your palette
       ↓
layout-validator ← Rough out your layout
       ↓
power-design-audit ← Validate against 10 rules
       ↓
awesome-design-lookup ← Reference specific patterns
       ↓
SHIP ✓
```

Not a strict pipeline — use skills in any order that fits your workflow.

---

## References & Sources

All skills are grounded in published design research:

- **Power Design** (20 principles): Edward Tufte, Garr Reynolds, Nancy Duarte, Robin Williams, Adam Wathan & Steve Schoger (Refactoring UI), Josef Müller-Brockmann, WCAG 2.2, Nielsen Norman Group
- **Awesome Design MD** (73 brands): Extracted from [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md)
- **Color Theory**: Itten 60-30-10 rule, WCAG contrast standards
- **Typography**: Butterick's Practical Typography, Bringhurst's Elements of Typographic Style
- **Layout**: F-pattern from Nielsen Norman Group eye-tracking studies, 8pt grid from Material Design

---

## Workflow: Landing Page Example

You're building a landing page in ClickFunnels or similar platform. Here's how the skills fit:

1. **design-extract** → "Show me how Stripe structures opt-in pages"
   - Get Stripe's color palette, CTA button style, form layout

2. **color-system-builder** → Input your brand color
   - Generate full palette ready for ClickFunnels

3. **layout-validator** → Describe hero + form + social proof
   - Check F-pattern, 8pt alignment, whitespace

4. **power-design-audit** → Describe your final layout
   - Validate against 10 rules before publishing

5. **awesome-design-lookup** → "How do fintech companies do trust sections?"
   - Reference Stripe, Coinbase, Wise approaches for social proof

**Total time:** 30 minutes planning, zero guessing.

---

## Sharing with Your Team

**Scenario:** You've finished a project using these skills and want to introduce the team to `power-design-audit`.

1. **Show, don't tell:** Use the skill in a team meeting, show the audit output
2. **Explain the principles:** "We're checking against 10 design principles from researchers like Tufte and Duarte"
3. **No mandates:** "This is optional — if it's useful, we can adopt it. If not, no worries"
4. **Start small:** Introduce 1–2 skills first (power-design-audit + color-system-builder are lowest-friction)
5. **Document:** If the team wants to adopt, create a shared guide with your preferred workflow

See `TEAM_SHARING.md` for templates and talking points.

---

## Troubleshooting

**Skills not appearing in Claude Code?**
- Verify clone path: `ls ~/.claude/skills/design-skills/` should list 5 .md files
- Restart Claude Code
- Try `/use power-design-audit` to trigger skill discovery

**Want to customize a skill for your workflow?**
- Edit the .md file directly in `~/.claude/skills/design-skills/[skill-name].md`
- Skills are just text — change whatever you want
- Commit changes to your fork if you want to track customizations

**Want to add a new skill?**
- Create `new-skill.md` in this repo
- Follow the structure of existing skills
- Test with `/use new-skill`
- Commit and push

**Team member wants to use a skill but doesn't have it?**
- Share the repo link or send them the INSTALLATION section
- They clone the same way, invokes the same skills

---

## Next Steps

1. **Clone the repo** (see Installation above)
2. **Test one skill** in Claude Code (suggest starting with `power-design-audit`)
3. **Use in your next project** and see how it changes your workflow
4. **Decide what to share with your team** (or keep for personal use — no pressure)
5. **Contribute back** if you improve any skill (git push to your fork, PR welcome)

---

## File Structure

```
design-skills/
├── README.md                    # This file
├── INSTALLATION.md             # Setup instructions (Claude Code, web, team)
├── TEAM_SHARING.md             # How to introduce tools to your team
│
├── claude-code/                # Claude Code skills
│   ├── power-design-audit.md
│   ├── color-system-builder.md
│   ├── design-extract.md
│   ├── layout-validator.md
│   └── awesome-design-lookup.md
│
├── templates/                  # Reusable templates (DESIGN.md, etc.)
├── reference/                  # Design principles, frameworks, research
├── web/                        # (Future) Web-based tools
├── figma/                      # (Future) Figma plugins
│
├── .gitignore
└── LICENSE
```

**Note:** Current focus is Claude Code skills. Easily extensible to web tools, Figma plugins, team documentation templates, etc.

---

## License

MIT — same as your other design projects. Use, modify, share as you see fit.

---

**Last Updated:** May 9, 2026  
**Author:** Keith Ratner  
**Status:** Ready for Production  
**Repo:** `https://github.com/kratner/design-skills`

For questions or improvements, open an issue or edit directly.
