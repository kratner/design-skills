# Extending Design Skills

This repo is built to grow beyond the initial 5 Claude Code skills. Here's how to add skills for other platforms and create new tools.

## Adding a New Claude Code Skill

### Quick Path (for you, Keith)

1. **Create the skill file:**
   ```bash
   cd ~/design-skills/claude-code
   nano my-new-skill.md
   ```

2. **Use existing skill as template** (copy power-design-audit.md structure):
   ```
   # Skill Name
   
   ## Purpose
   [What it does in one sentence]
   
   ## How to Use
   ```
   /use my-new-skill
   [Describe what user provides]
   ```
   
   ## What You Get
   [Describe output]
   
   ## When to Use
   [Describe use cases]
   ```

3. **Copy to Claude Code directory:**
   ```bash
   cp my-new-skill.md ~/.claude/skills/design-skills/
   ```

4. **Test in Claude Code:**
   ```
   /use my-new-skill
   ```

5. **Commit:**
   ```bash
   git add claude-code/my-new-skill.md
   git commit -m "Add: my-new-skill for [use case]"
   git push
   ```

## Adding a New Platform Tool

### Web-Based Tool

Example: A web tool for validating color contrast interactively.

```
design-skills/web/
├── README.md                    # How to use the web tool
├── index.html                   # Main page
├── contrast-validator.js        # Tool logic
├── styles.css
└── utils.js
```

**Add it:**
1. Create `design-skills/web/contrast-validator/` folder
2. Add `README.md` with instructions
3. Commit: `git add web/contrast-validator && git commit -m "Add: web contrast validator"`

### Figma Plugin

Example: A Figma plugin that checks designs against Power Design rules.

```
design-skills/figma/
├── README.md                    # Installation + usage
├── manifest.json                # Figma plugin config
├── code.js                      # Plugin logic
└── ui.html                      # UI
```

**Add it:**
1. Create `design-skills/figma/[plugin-name]/` folder
2. Add manifest.json + code
3. Commit: `git add figma/[plugin-name] && git commit -m "Add: Figma [plugin-name]"`

### Shared Documentation / Templates

Example: A DESIGN.md template for team projects.

```
design-skills/templates/
├── DESIGN.md                    # Base template
├── DESIGN.landing-page.md       # Landing page variant
└── DESIGN.app.md                # App variant
```

**Add it:**
1. Create `design-skills/templates/[template-name].md`
2. Include full YAML structure, examples
3. Commit: `git add templates/[template-name].md && git commit -m "Add: [template-name] template"`

## Skill Ideas (Roadmap)

These are skills/tools worth building:

### Claude Code Skills (v1.1)
- `design-compare` — Compare your design against 2–3 reference brands
- `typography-scale` — Generate modular type scales (1.25, 1.618 ratios)
- `spacing-validator` — Audit project's spacing against 8pt grid
- `wcag-validator` — Check color contrast + readability rules

### Web Tools (v1.2)
- Interactive contrast checker (input hex, see AA/AAA pass/fail)
- Color system generator (visual interface, export CSS variables)
- F-pattern diagram builder (sketch layout, get feedback)
- 60-30-10 palette visualizer (drag colors, see composition)

### Figma Plugins (v1.3)
- Auto-check designs against Power Design rules (live in Figma)
- Color system generator (plugin version)
- Spacing validator (audit frames + layers)
- Accessibility checker (contrast, text sizes, etc.)

### Team Documentation (ongoing)
- DESIGN.md templates for different project types
- Design principle guides (simplified for team use)
- Component libraries (button, card, form patterns)

## Naming Conventions

To keep the repo organized as it grows:

**Files:**
- Claude Code skills: `claude-code/[skill-name].md`
- Web tools: `web/[tool-name]/index.html` (+ supporting files)
- Figma plugins: `figma/[plugin-name]/manifest.json` (+ code.js, ui.html)
- Templates: `templates/[purpose].md` (e.g., DESIGN.landing-page.md)
- Reference docs: `reference/[topic].md` (e.g., power-design-rules.md)

**Git commits:**
- New Claude Code skill: `Add: [skill-name] for [use case]`
- New web tool: `Add: web [tool-name]`
- New template: `Add: [template-name] template`
- Updates: `Update: [skill/tool] — [change description]`

## PR / Contribution Guidelines

If you fork this repo or want to suggest additions:

1. **Fork the repo**
2. **Create a feature branch:** `git checkout -b feature/my-new-skill`
3. **Add your skill:**
   - For Claude Code: add to `claude-code/`
   - For web: add to `web/[name]/`
   - For templates: add to `templates/`
4. **Update README** with new skill in appropriate section
5. **Test thoroughly** before submitting
6. **Commit with clear message:** `Add: [skill-name] for [purpose]`
7. **Push and create a PR**

---

## Adding to the README

When you add a new skill/tool, update README.md:

**For Claude Code skill:**
```markdown
### N. **skill-name**
Brief description of what it does.

**Use when:**
- Scenario 1
- Scenario 2

**Example:** `/use skill-name` → Input X → Get Y
```

**For web tool:**
```markdown
### Web: Tool Name
What it does. How to access (local, URL, etc.).

**Use when:** Scenarios
```

**For Figma plugin:**
```markdown
### Figma: Plugin Name
What it does. Installation instructions.

**Use when:** Scenarios
```

## Future Structure (When Large)

Once the repo grows beyond 10 skills:

```
design-skills/
├── claude-code/
│   ├── validation/              # power-design-audit, layout-validator, etc.
│   ├── generation/              # color-system-builder, design-extract, etc.
│   └── reference/               # awesome-design-lookup, etc.
├── web/
│   ├── validators/              # contrast checker, spacing validator
│   ├── generators/              # color system builder, type scale generator
│   └── visualizers/             # palette visualizer, F-pattern builder
├── figma/
│   ├── validators/
│   ├── generators/
│   └── helpers/
├── templates/
├── reference/
└── docs/                        # Extended documentation
```

For now, flat structure is fine. Refactor when needed.

---

## Questions?

- How to add a skill? → Copy an existing `.md` file, edit, test, commit
- How to add a web tool? → Create folder in `web/`, add HTML + JS, update README
- How to add a Figma plugin? → Create folder in `figma/`, add manifest.json + code.js
- How to suggest an idea? → Open an issue or create a PR with skeleton files

**Status:** Open to contributions. Maintain the philosophy: evidence-based, practical, minimal, reusable.

---

**Last Updated:** May 9, 2026  
**Next Update:** When first new skill is added (v1.1)
