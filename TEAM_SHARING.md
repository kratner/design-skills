# Sharing Design Skills with Your Team

This file helps you decide which skills to share, when, and how to introduce them without mandating.

## Philosophy

These are **your tools** for personal use and your team's **optional reference**. No tool, process, or framework is universal — the goal is to offer proven approaches and let your team decide if they're useful.

## Which Skills Are Most Team-Friendly?

### Tier 1: Safe to Introduce (Low Friction)

These are self-explanatory and don't require a philosophy shift. Good for any team context:

**power-design-audit**
- What: Checklist against 10 design principles
- Why team might like it: Fast validation, specific feedback
- Barrier: None. It's optional, grounded in published research, no ideology
- Best intro: Show a completed audit, let them ask questions
- Time to understand: 10 minutes

**color-system-builder**
- What: Generate a full color palette from one hex value
- Why team might like it: Fast, removes guessing, ensures contrast compliance
- Barrier: None. It's a tool, no philosophy required
- Best intro: "Here's how I generate consistent color systems now"
- Time to understand: 5 minutes

### Tier 2: Useful but Requires Context (Medium Friction)

These work best when explained alongside the principles they enforce:

**layout-validator**
- What: Check if layout follows F-pattern, 8pt grid, whitespace ratios
- Why team might like it: Catches structural issues early
- Barrier: May feel prescriptive ("why does it have to be 8pt?")
- Best intro: Show a layout that failed, got fixed, then passed
- Time to understand: 20 minutes (need to explain why these principles matter)

**design-extract**
- What: Pull design DNA from a brand and adapt it
- Why team might like it: Fast reference, avoids reinventing the wheel
- Barrier: Might feel like copying instead of innovating
- Best intro: "We're studying how Stripe/Notion solve this problem, then we adapt"
- Time to understand: 15 minutes

### Tier 3: Keep for Yourself (High Friction)

These are deep reference tools, not team-facing:

**awesome-design-lookup**
- What: Reference 73 brands' design systems
- Why you use it: Daily inspiration, comparative analysis
- Why team doesn't need it: They can ask you if they want to study a brand
- Best approach: You use it silently, surface insights when relevant
- Example: You research how Notion does buttons, then show the team your recommendation

---

## Suggested Introduction Timeline

### Week 1: Show, Don't Teach

In your first meeting or Slack conversation:

**What to do:**
- Share a screenshot of `power-design-audit` output from a ClickFunnels page you designed
- Say: "I'm using a framework to validate designs against 10 principles from research. Here's what it caught. Interested?"

**What to expect:**
- Curiosity, skepticism, or indifference. All are fine.
- Maybe 1–2 people ask questions.

**What NOT to do:**
- Don't present it as "better than how we work now"
- Don't suggest they need to adopt it
- Don't make it about enforcing rules

---

### Week 2–3: One-on-One Opt-In

If someone shows interest:

**What to do:**
- Offer to walk them through `color-system-builder` or `power-design-audit` on a project they're working on
- Let them experience the workflow: input → output → "Oh, that's useful"

**What to expect:**
- Some people will want to try it, some won't. Both are fine.
- If someone tries it, ask: "Was that helpful? Any feedback?"

---

### Month 2+: Organic Adoption

If people are using the skills:

**What to do:**
- Create a shared doc: "Design Framework Keith Uses" with one-page summaries
- Share the GitHub repo link in case people want to clone locally
- Mention how you're using the skills in your own work (landing pages, projects, etc.)

**What NOT to do:**
- Don't make it a process requirement
- Don't grade designs based on the 10 rules
- Don't suggest people who don't use it are doing it wrong

---

## Template: How to Introduce a Skill in a Meeting

Pick the skill tier and use this structure:

### Tier 1 (Safe) Example: Introducing color-system-builder

```
"Hey team, I wanted to show you something I've been using. 
[Show a screenshot of input + output]

This is a tool that takes one color (like a brand color) and 
generates a full system: backgrounds, text, accents, everything 
validated for contrast.

It saves me ~30 minutes per project, and I always hit WCAG AA 
without thinking about it. 

Might be useful for anyone building in ClickFunnels, or it might 
not be — depends on your workflow. Wanted to show you in case it's 
interesting."

[Answer questions if they have them]
[Drop the repo link in Slack: github.com/kratner/design-skills]
```

### Tier 2 (Context-Needed) Example: Introducing layout-validator

```
"Quick design talk: I've been testing layouts against something 
called the F-pattern — basically, how users naturally scan a page.

[Show two layouts: one passes, one fails]

Left-side anchor, natural reading flow, good whitespace — it catches 
a lot of issues before we even build.

No pressure to use it, but if you ever get feedback like 'something 
feels off' and you're not sure why, this framework can help diagnose.

Happy to walk anyone through it who's curious."
```

---

## Red Flags: When NOT to Push a Skill

❌ Don't introduce a skill if:
- You're frustrated with a design someone made ("They should have used power-design-audit")
- You're trying to enforce consistency through tools
- You're implying current designs are wrong
- You've only used it once yourself
- You can't articulate why it matters in 1–2 sentences

✅ Do introduce a skill if:
- You've used it successfully on 2+ projects
- It genuinely saved you time or caught a real problem
- Someone asks you how you did something
- You can explain it without sounding like you're preaching
- You're excited about it (enthusiasm is contagious)

---

## If Someone Asks: "Why Is This Better?"

**Don't say:** "Because these are based on research"  
**Do say:** "These principles come from people like Edward Tufte and Garr Reynolds who study how humans see and read. I use them as a checklist — saves me time, catches stuff I'd miss."

**Don't say:** "You should use this"  
**Do say:** "I found this helpful for [specific problem]. Might work for you, might not."

**Don't say:** "This is the right way to design"  
**Do say:** "This is one framework. Plenty of great design doesn't follow every rule."

---

## If Someone Adopts a Skill

Great! Here's what to do:

1. **Don't hover:** They'll figure out how to use it.
2. **Ask for feedback:** "How's the tool working for you?"
3. **Share tips if they ask:** "One thing I do is [use case]"
4. **Celebrate quietly:** No need to make a big deal.
5. **Document together:** If they suggest improvements, maybe add to the repo.

---

## If Someone Ignores a Skill

That's fine. Some people:
- Prefer intuition over frameworks
- Don't like validating against checklists
- Have their own proven process
- Just haven't had time to learn something new

**Respect that.** Your job is to offer the tool, not mandate its use.

---

## Shared Collaboration Integration

You work with a team on shared projects. Here's how to integrate design skills naturally:

**Scenario 1: You finish a project**
- Share the project + a `DESIGN.md` file in your shared space
- Include a link to the power-design-audit results (if you want)
- Someone curious will ask: "How did you do that?"

**Scenario 2: Team collaborates on a design**
- You suggest using design-extract to research how similar brands solve the problem
- Drop the repo link in the shared doc
- Let people explore at their own pace

**Scenario 3: Someone asks for design advice**
- You can offer to run color-system-builder or power-design-audit for them
- Or teach them how to do it themselves
- Or just share the results

---

## What NOT to Do in Team Spaces

❌ Don't:
- Post validation results with a lecture
- Suggest people use a skill "correctly"
- Create a mandatory DESIGN.md requirement
- Make it feel like there's one way to do things

✅ Do:
- Share tools openly and assume people are smart
- Answer questions if they ask
- Show your work (how you built something)
- Let people opt in

---

## If Your Team Wants to Adopt the Framework

If the team says "We like this, let's use it," here's a path:

1. **Document your current workflow** in a shared doc
2. **Create a team guide** with simplified explanations
3. **Define which skills are required vs. optional** (suggest: none required, all optional)
4. **Set up a feedback loop:** Periodic check-ins: "How's this working for everyone?"
5. **Stay flexible:** Rules should serve the team, not the other way around

See next section for a template team guide.

---

## Template: Team Guide (If They Want It)

If your team asks to adopt the design skills officially:

```markdown
# Team Design Framework

We use evidence-based design principles to validate designs 
before launch. Framework is optional — it's a checklist, not law.

## Quick Start

- Clone repo: [link]
- Use in Claude Code: `/use power-design-audit`

## When to Use

**color-system-builder:** Starting a new project or brand
**power-design-audit:** Before finalizing a layout
**design-extract:** Researching how competitors structure designs
**layout-validator:** Catching structure issues early

## Team Guidelines

1. Tools are optional. Use if helpful, ignore if not.
2. No design is "wrong" if it breaks a rule — rules are heuristics.
3. Feedback is about principles, not taste.
4. Questions? Check the documentation or ask.

## Feedback

Using these tools? We'd love to know what's working, what's not.
Share feedback in your team communication channel.
```

---

## Key Takeaway

**You're not enforcing rules.** You're offering proven frameworks that save time and catch issues. People will use them if they're useful. Trust that.

If someone says "This isn't for me," that's a valid choice. No hard feelings.

---

**Last Updated:** May 9, 2026  
**For:** Keith Ratner  
**Status:** Guidance Document
