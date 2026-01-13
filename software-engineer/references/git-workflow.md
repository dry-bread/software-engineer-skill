# Git Workflow

Version control practices and submission process for this project.

---

## Workflow: Git Process

### Main Branch

**Primary branch:**

*This section will be populated after analyzing repository.*

---

### Branch Naming

**Branch naming conventions:**

*This section will be populated after analyzing git history.*

---

### Commit Message Format

**Commit message conventions:**

*This section will be populated after analyzing commit history.*

---

### Pull Request Process

**How to create and submit PRs:**

*This section will be populated after first PR or analyzing templates.*

---

### Code Review Process

**Review requirements and approval process:**

*This section will be populated after observing review practices.*

---

### Merge Strategy

**How PRs are merged:**

*This section will be populated after observing merge patterns.*

---

## Workflow: When Git Workflow is Empty

**If sections above are empty:**

```
WORKFLOW:
1. Check repository configuration
   
   a. Check main branch:
      git branch --show-current
      git remote show origin | grep "HEAD branch"
   
   b. Review recent commits:
      git log --oneline -20
      → Observe commit message patterns
   
   c. Review existing branches:
      git branch -a
      → Observe branch naming patterns

2. Look for documentation
   
   a. Check for CONTRIBUTING.md
   b. Check for .github/pull_request_template.md
   c. Check for .github/PULL_REQUEST_TEMPLATE/
   d. Check for docs/git-workflow.md or similar

3. If documentation found:
   
   Extract and propose:
   "Found git workflow documentation in [source]:
   - Main branch: [name]
   - Branch naming: [pattern]
   - Commit format: [pattern]
   - PR template: [exists/doesn't exist]
   
   Should I populate git-workflow.md with these conventions?"

4. If no documentation found:
   
   Infer from repository:
   "No git workflow documented. Based on repository analysis:
   - Main branch appears to be: [main/master/develop]
   - Recent commits use format: [observed pattern]
   - Branch names follow: [observed pattern or 'no clear pattern']
   
   What are your preferred git conventions?"

5. After first successful PR submission:
   
   - Document all steps actually taken
   - Record branch name format used
   - Record commit message format used
   - Record PR description format
   - Populate sections above
```

---

## Workflow: During Code Submission

**While submitting code (Stage 6), observe and learn:**

```
WORKFLOW:
1. Create branch
   
   a. Check documented branch naming (sections above)
   b. If documented → Follow the pattern
   c. If not documented → Ask user for branch name format
   d. Create branch with chosen name

2. Commit changes
   
   a. Check documented commit format (sections above)
   b. If documented → Follow the format
   c. If not documented → Ask user for commit message format
   d. Make commit with chosen format

3. Push and create PR
   
   a. Check documented PR process (sections above)
   b. If PR template exists → Use it
   c. If not documented → Ask user for PR description format
   d. Create PR with appropriate description

4. Observe user corrections
   
   Track when user changes:
   - Branch name → "You changed branch to [X]. Should this be the standard?"
   - Commit message → "You edited commit to [X]. Should I use this format next time?"
   - PR description → "You modified PR description. Should I update the template?"
   
   If user corrects twice → Process pattern detected
   → Ask: "Should I document '[correction]' as the standard practice?"

5. Observe merge process
   
   After PR is merged:
   - How was it merged? (merge commit / squash / rebase)
   - Were there review requirements?
   - Was PR template followed?
   
   → Document observed merge strategy

6. Update git-workflow.md
   
   After successful submission:
   - If sections were empty → Populate with what worked
   - If practice differs from docs → Propose update
   - If new pattern observed → Propose adding
```

