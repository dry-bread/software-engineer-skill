---
name: software-engineer
description: Standardized software engineering workflow for code modification, debugging, testing, and submission within a codebase. Use when asked to add features, fix bugs, investigate issues, refactor code, or complete any code-related engineering task. Triggers include requests to modify code, run projects, debug errors, locate problems, understand business logic, submit PRs, or review code changes.
---

# Software Engineer

A structured workflow skill for systematic code repository work, from understanding requirements through code submission.

## Core Workflow

Follow this 6-stage process for all code engineering tasks:

### Stage 1: Understand Requirements

**Actions:**
1. Parse user request to identify the task type:
   - Feature addition
   - Bug fix
   - Investigation/debugging
   - Refactoring
   - Other modifications
2. Clarify ambiguous requirements with targeted questions
3. Load [references/codebase-context.md](references/codebase-context.md) to understand project context

**Quality Gate:** Clear understanding of what needs to be done and why.

---

### Stage 2: Analyze Code

**Actions:**
1. Locate relevant files using semantic search or file search
2. Read code to understand current implementation
3. Compare requirements against existing logic
4. Identify potential issues or gaps in requirements
5. Trace dependencies and impact scope

**When to load references:**
- **Always load** [references/codebase-context.md](references/codebase-context.md) if not already loaded
- For understanding business logic and module relationships
- **Load specific feature docs** from [references/features/](references/features/) when user mentions a feature by name

**Quality Gate:** Comprehensive understanding of code structure and impact scope.

---

### Stage 3: Propose Solution

**Actions:**
1. Design modification approach considering:
   - Business logic clarity
   - Code style consistency
   - Minimal impact scope
   - Maintainability
2. Present solution plan to user
3. Discuss alternatives if multiple approaches exist
4. Get user confirmation before proceeding

**Quality Gate:** User-approved solution plan.

---

### Stage 4: Modify Code

**Actions:**
1. **Load** [references/coding-standards.md](references/coding-standards.md) before making changes
2. Implement changes following project conventions:
   - Match existing code style
   - Use preferred packages and patterns
   - Follow naming conventions
   - Maintain consistent formatting
3. Ensure business logic remains clear and testable
4. Validate syntax and imports

**Quality Gate:** Code changes complete, style-consistent, and error-free.

---

### Stage 5: Run & Test

**Actions:**
1. **Load** [references/run-guide.md](references/run-guide.md)
2. Execute project according to run instructions
3. Verify changes work as expected
4. Debug any runtime errors
5. Invite user to test the changes
6. Iterate based on test feedback

**Quality Gate:** Changes verified working by both automated execution and user testing.

---

### Stage 6: Submit & Summarize

**Actions:**
1. **Load** [references/git-workflow.md](references/git-workflow.md)
2. Create feature branch following naming conventions
3. Commit changes with proper message format
4. Push to remote repository
5. Generate comprehensive change summary including:
   - Modified files
   - Key changes description
   - Impact analysis
   - Testing notes
6. Format as PR description if applicable

**Quality Gate:** Code submitted with clear documentation.

---

## Decision Tree

```
User Request
    ├─ "Add feature" → Stage 1-6 (full workflow)
    ├─ "Fix bug" → Stage 1-6 (full workflow)
    ├─ "Investigate issue" → Stage 1-2, then report findings
    ├─ "Run project" → Jump to Stage 5
    ├─ "Explain code" → Stage 2 only, load codebase-context.md
    ├─ "Review changes" → Load git-workflow.md, analyze diff
    └─ "Retrospective" → Load references/retrospective-guide.md
```

## Checkpoints

Use these to verify quality at each stage:

- [ ] Requirements clear and confirmed
- [ ] Code impact scope identified
- [ ] Solution approach approved by user
- [ ] Changes follow project coding standards
- [ ] Code tested and verified working
- [ ] Changes properly committed and documented

## Optional Advanced References

Load these when explicitly needed:

- **references/retrospective-guide.md** - For post-work analysis and improvement identification
- Additional references can be added as the skill evolves

## Key Principles

1. **Always confirm before coding** - Get user approval on approach (Stage 3)
2. **Load standards before modifying** - Ensure consistency with existing code
3. **Test before submitting** - Never submit untested changes
4. **Document comprehensively** - Future developers (including you) will thank you
