# Retrospective Guide

Conduct retrospectives after completing tasks to improve work quality and skill effectiveness.

---

## Workflow: Conducting Retrospectives

### When to Conduct

**Quick retrospective (2 minutes):**
- After every task completion
- Focus on key learnings

**Full retrospective:**
- Complex multi-file changes
- When things went wrong
- When user explicitly requests
- After major milestones

---

### Step 1: Interaction Retrospective

**Analyze the conversation efficiency:**

```
Questions to ask:
- Was the requirement clear from the start?
- How many clarification rounds were needed?
- Were the right files/tools accessed?
- Could we have reached the solution faster?

Learning:
- What questions should have been asked earlier?
- What assumptions were made that caused delays?
```

**Output format:**
```markdown
**Interaction Analysis:**
- Clarity: [Clear / Required X clarifications]
- Efficiency: [Could improve by: ...]
- Key learning: [...]
```

---

### Step 2: Code Change Retrospective

**Analyze the implementation quality:**

```
Questions to ask:
- Is this the best approach?
- Did we modify all necessary files?
- What edge cases might break this?
- What testing gaps remain?
- What technical debt was created?

Learning:
- What patterns emerged from this codebase?
- What could be improved in the solution?
- What should be refactored later?
```

**Output format:**
```markdown
**Code Quality Analysis:**
- Solution approach: [Description]
- Completeness: [All files modified / Missing: ...]
- Technical debt: [None / List items]
- Patterns learned: [...]
```

---

### Step 3: Skill Documentation Retrospective

**Analyze whether skill's reference files helped or hindered:**

#### 3.1 Check Each Reference File

**For each reference file that was loaded:**

| Reference File | Accurate? | Helpful? | Needs Update? | Notes |
|----------------|-----------|----------|---------------|-------|
| codebase-context.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| coding-standards.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| run-guide.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| git-workflow.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| features/[X].md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |

#### 3.2 Stage-by-Stage Friction Analysis

**Check each workflow stage:**

```
Stage 1 (Understand Requirements):
- Was codebase-context.md loaded?
- Did it have the business context needed?
- What information was missing?
- Did feature documentation exist and help?

Stage 2 (Analyze Code):
- Were feature docs accurate?
- Did they match actual code?
- What gaps were discovered?

Stage 4 (Modify Code):
- Was coding-standards.md loaded?
- Did it reflect actual code patterns?
- What undocumented standards were found?

Stage 5 (Run & Test):
- Was run-guide.md loaded?
- Did it have the commands needed?
- What missing steps were encountered?

Stage 6 (Submit):
- Was git-workflow.md loaded?
- Did it match repository conventions?
- What conflicts between docs and practice?
```

#### 3.3 Detect Repeated Patterns

**Check for information searched multiple times:**

```
Questions:
- What information did I search for in this task?
- Have I searched for similar information before?
- Is there a pattern worth documenting?

Examples:
- Searched for authentication logic 3 times → Document in features/
- Had to figure out run commands again → Update run-guide.md
- User corrected branch naming twice → Update git-workflow.md
```

#### 3.4 Identify Learning Opportunities

**Capture new patterns discovered:**

```
For each new pattern:
- What pattern did I learn about this codebase?
- Where should it be documented?
- How would it help future tasks?

Template:
Pattern: [Description of what was learned]
Document in: [Which reference file]
Benefit: [How this speeds up future work]
```
