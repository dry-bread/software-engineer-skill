# Git Workflow

Version control practices, branching strategy, and commit guidelines for this project.

---

## 🔄 Self-Improvement Guide

**When to update this file:**
- Load this file at Stage 6 (Submit & Summarize)
- When git conventions are unclear or undocumented
- When user corrects branch naming or commit format

**Signals that trigger updates:**

1. **File is empty or has placeholders**
   - Check .git config for branch info (main/master)
   - Review existing commits for message patterns (git log)
   - Look for CONTRIBUTING.md or .github/pull_request_template.md
   - Ask user: "Git workflow not documented. What's your main branch and preferred commit format?"

2. **Documented practice conflicts with repository**
   - Observe actual branch naming in git history
   - Check actual commit message formats
   - Ask user: "Repo uses [pattern X] but git-workflow says [pattern Y]. Which should I follow? Update docs?"

3. **User corrects during submission**
   - User provides different branch name format
   - User changes commit message
   - User specifies different PR process
   - Ask user: "Should I add '[your correction]' to git-workflow.md for next time?"

4. **PR template exists but not documented**
   - Find PR templates in .github/
   - Incorporate into workflow documentation

**Update proposal format:**
```
**Git Workflow Improvement**

Current documentation: [What git-workflow.md says or is missing]
Observed practice: [What repository actually uses]
User correction: [What user just told me]

Proposed update to git-workflow.md:
- Update: [Specific field like branch naming, commit format]
- From: [Old or missing]
- To: [New standard]

Should I update the workflow documentation?
```

**What to observe in repository:**
- Main branch name (main/master/develop)
- Branch naming patterns (feature/, bugfix/, hotfix/)
- Commit message format (conventional commits, simple messages)
- PR description templates
- Merge strategy (merge commits, squash, rebase)

---

## How to Use This File

**This file is initially empty.** It learns from your repository:

1. **First PR** - Observes git history and .github/ templates
2. **Proposes workflow** - Based on actual repository patterns
3. **Tracks deviations** - When documented workflow differs from practice

**Content will include:**
- Branch naming conventions
- Commit message format
- PR creation process
- Code review guidelines
- Merge strategies

---

## Content Sections (Populated During Use)

**The skill will add these sections as needed:**

- **Branch Naming** - Conventions for feature/bugfix/hotfix branches
- **Commit Messages** - Format and best practices
- **Pull Request Process** - How to create and structure PRs
- **Code Review** - Review checklist and approval process
- **Merge Strategy** - Merge vs rebase vs squash

---

**Note:** This is a living document. It learns from actual git history and adapts to repository conventions.
