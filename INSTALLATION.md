# Installation & Setup Guide

## For Keith (Personal Use)

### Quick Setup (2 minutes)

```bash
# Clone the repo into your Claude Code skills directory
git clone https://github.com/kratner/design-skills ~/.claude/skills/design-skills

# Verify installation
ls ~/.claude/skills/design-skills/*.md
# Should list: power-design-audit.md, color-system-builder.md, etc.
```

### Test It Works

In Claude Code, type:
```
/use power-design-audit
```

You should see the skill load. If not, restart Claude Code and try again.

### Keep It Updated

```bash
cd ~/.claude/skills/design-skills
git pull origin main
```

Run this whenever you want the latest version (or set a monthly reminder).

---

## For Ace Media Team (Optional, Individual Setup)

### Each Team Member: 5-Minute Setup

If a team member wants to use design skills:

1. **They clone the repo:**
   ```bash
   git clone https://github.com/kratner/design-skills ~/.claude/skills/design-skills
   ```

2. **They test in Claude Code:**
   ```
   /use power-design-audit
   ```

3. **They're done.** No config, no dependencies, no special setup.

### Share This Link

Drop this in Slack / shared doc so people can self-serve:

```
Want to try design skills? 
1. Run: git clone https://github.com/kratner/design-skills ~/.claude/skills/design-skills
2. In Claude Code, type: /use power-design-audit
3. Done! Ask Keith if you have questions.
```

---

## For GitHub (If Creating a Public Repo)

### Initial Setup

```bash
cd ~/design-skills

# Initialize git (if not already done)
git init
git config user.name "Keith Ratner"
git config user.email "admin@entremax.media"

# Add all files
git add .

# First commit
git commit -m "Initial commit: Five design skills for evidence-based design"

# Connect to GitHub (create repo at github.com/kratner/design-skills first)
git remote add origin https://github.com/kratner/design-skills.git
git branch -M main
git push -u origin main
```

### Ongoing Updates

```bash
cd ~/design-skills
git add [changed files]
git commit -m "Update: [what changed]"
git push
```

---

## Troubleshooting

### Skills Not Appearing in Claude Code

**Problem:** `/use power-design-audit` returns "skill not found"

**Fix 1: Verify path**
```bash
ls ~/.claude/skills/design-skills/
```
Should list: `power-design-audit.md`, `color-system-builder.md`, etc.

If not, git clone didn't work. Try again:
```bash
rm -rf ~/.claude/skills/design-skills
git clone https://github.com/kratner/design-skills ~/.claude/skills/design-skills
```

**Fix 2: Restart Claude Code**
- Quit Claude Code completely
- Reopen
- Try `/use power-design-audit` again

**Fix 3: Check Claude Code version**
Skills require Claude Code recent build. If you're on an old version:
- Update Claude Code from the App Store
- Try again

### Can't Clone the Repo

**Problem:** `git clone` says "repository not found"

**Reason 1: GitHub repo doesn't exist yet**
- Create it at github.com/kratner/design-skills
- Then retry clone

**Reason 2: SSH key issue**
```bash
# Use HTTPS instead of SSH
git clone https://github.com/kratner/design-skills.git ~/.claude/skills/design-skills
```

**Reason 3: Wrong GitHub URL**
- Double-check: github.com/kratner/design-skills
- Not a fork, not a typo

### Git Pull Shows Merge Conflicts

**Problem:** `git pull` says "conflict in [file]"

**Reason:** You edited a skill file locally, and the remote also changed

**Fix:**
```bash
cd ~/.claude/skills/design-skills

# Option 1: Keep your local version
git checkout --ours power-design-audit.md
git add .
git commit -m "Resolved: keeping local version"

# Option 2: Use remote version (loses your edits)
git checkout --theirs power-design-audit.md
git add .
git commit -m "Resolved: using remote version"
```

If you've customized skills, consider forking the repo so you don't have conflicts.

### Skills Load but Return Errors

**Problem:** `/use power-design-audit` loads, but Claude returns an error

**Reason:** The skill's `.md` file is malformed or Claude can't parse it

**Fix:**
1. Check file exists: `cat ~/.claude/skills/design-skills/power-design-audit.md`
2. File should start with clear instructions, not code
3. If file is empty or corrupted, re-clone: `rm -rf ~/.claude/skills/design-skills && git clone ...`

---

## Customization

### Edit a Skill

All skills are plain `.md` files. You can edit directly:

```bash
# Edit in your favorite editor
nano ~/.claude/skills/design-skills/power-design-audit.md

# Test changes immediately in Claude Code
# /use power-design-audit
```

### Create a New Skill

1. **Copy an existing skill:**
   ```bash
   cp ~/.claude/skills/design-skills/power-design-audit.md \
      ~/.claude/skills/design-skills/my-new-skill.md
   ```

2. **Edit the file:**
   ```bash
   nano ~/.claude/skills/design-skills/my-new-skill.md
   ```

3. **Update the first section** (Purpose, How to Use)

4. **Test in Claude Code:**
   ```
   /use my-new-skill
   ```

5. **Commit if happy:**
   ```bash
   cd ~/.claude/skills/design-skills
   git add my-new-skill.md
   git commit -m "Add: my-new-skill"
   git push
   ```

### Fork for Team Customization

If Ace Media wants to customize skills for your team:

1. **Fork on GitHub** (creates your own copy)
2. **Clone your fork:** 
   ```bash
   git clone https://github.com/[your-github]/design-skills.git \
     ~/.claude/skills/design-skills
   ```
3. **Customize .md files** (edit directly)
4. **Push changes to your fork:**
   ```bash
   git add .
   git commit -m "Team customization: [changes]"
   git push
   ```
5. **Share fork link** with team

---

## Dependencies

**Good news:** Skills have zero dependencies.

- No npm packages
- No build process
- No special libraries
- No Python, Ruby, or Node required

All you need:
- Git (to clone)
- Claude Code
- A terminal

---

## File Structure After Installation

After successful setup, you'll have:

```
~/.claude/skills/design-skills/
├── README.md
├── INSTALLATION.md
├── TEAM_SHARING.md
├── power-design-audit.md
├── color-system-builder.md
├── design-extract.md
├── layout-validator.md
├── awesome-design-lookup.md
├── .gitignore
├── LICENSE
└── .git/                    (git metadata)
```

All `.md` files are skills. They'll auto-load in Claude Code.

---

## Updating Claude Code

Skills work best on recent Claude Code versions. If you're on an older version:

```bash
# Check your version
claude --version

# Update (Mac)
softwareupdate -i -a

# Or download fresh from claude.com/code
```

Then restart Claude Code and test: `/use power-design-audit`

---

## Uninstalling

If you want to remove skills:

```bash
rm -rf ~/.claude/skills/design-skills
```

That's it. No cleanup required.

---

## Getting Help

**Skills aren't loading?**
- Check installation section above
- Try the troubleshooting steps
- Restart Claude Code

**Want to customize skills?**
- Edit the `.md` file directly
- Test in Claude Code
- Ask Claude Code for help with questions

**Want to share with team?**
- See TEAM_SHARING.md
- Provide the GitHub link
- Each person follows "For Ace Media Team" section above

---

## Next Steps

1. ✅ Clone the repo (see Quick Setup above)
2. ✅ Test one skill in Claude Code
3. ✅ Read README.md for skill descriptions
4. ✅ Use in your next ClickFunnels project
5. ✅ (Optional) Share with team if helpful

---

**Status:** Ready to Use  
**Last Updated:** May 9, 2026  
**Questions?** Check README.md or TEAM_SHARING.md
