# Git Workflow

Version control practices and submission process for this project.

---

## Workflow: Git Process

**Primary branch:** main

**Branch naming conventions:** `manting/{key word for code change}`

**Commit message conventions:**


### Pull Request Process

**How to create and submit PRs:**
1. First, read through the code you've modified and summarize what it does.
2. Pull the main branch, ensuring your local main branch has the latest code.
3. Based on what this code does, choose a concise and clear name for the new branch. Add a `manting/` prefix to the new branch name.
4. Create the branch and switch to it.
5. Commit the current changes to the new branch, using a commit message that concisely and clearly describes what these changes do.
6. Push the new branch to the remote repository.

### Code Review Process

**Review requirements and approval process:**

*This section will be populated after observing review practices.*


### Merge Strategy

**How PRs are merged:**

*This section will be populated after observing merge patterns.*


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

