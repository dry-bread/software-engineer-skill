# Retrospective Guide

After completing each task, conduct a brief retrospective to improve:

1. **Work quality** - How well was the task completed?
2. **Skill effectiveness** - Did the skill's documentation help or hinder?

---

## 🔄 Self-Improvement Guide

**When to update this file:**
- When conducting retrospectives after tasks
- When user feedback suggests retrospective process improvements
- When repeated patterns indicate missing analysis frameworks

**Signals that trigger updates:**

1. **Retrospective feels incomplete**
   - User says "we should also check [X]"
   - Important aspects not covered by current framework
   - Propose adding new analysis section

2. **Skill documentation analysis reveals gaps**
   - If multiple retrospectives find same skill files unhelpful
   - Specific reference files repeatedly need updates
   - Learning opportunities not captured

3. **User repeatedly asks for same retrospective info**
   - Missing standardized questions
   - Propose adding to framework

**Update proposal format:**
```
**Retrospective Guide Improvement**

Observed pattern: [What's missing or ineffective]
Occurred in: [Tasks where this was noticed]

Proposed update to retrospective-guide.md:
- [Section to add/modify]
- [New analysis framework or questions]

Should I add this to the retrospective framework?
```

---

## When to Conduct Retrospectives

**After every task completion:**
- Quick 2-minute review
- Focus on key learnings

**Full retrospective triggers:**
- Complex multi-file changes
- When things went wrong
- When user explicitly requests
- After major milestones

---

## Retrospective Framework

### 1. Interaction Retrospective

**Analyze the conversation:**

- **Clarity:** Was the requirement clear from the start?
- **Questions:** How many clarification rounds needed?
- **Tool Usage:** Were the right files/tools accessed?
- **Efficiency:** Could we have reached the solution faster?

**Learning:**
- What questions should have been asked earlier?
- What assumptions were made?

---

### 2. Code Change Retrospective

**Analyze the implementation:**

- **Solution Quality:** Is this the best approach?
- **Code Coverage:** Did we modify all necessary files?
- **Edge Cases:** What scenarios might break this?
- **Testing:** What testing gaps remain?

**Learning:**
- What patterns emerged?
- What could be improved?
- What technical debt was created?

---

### 3. Skill Documentation Retrospective

**Analyze skill effectiveness:**

**Documentation Accuracy:**

| Reference File | Accurate? | Helpful? | Needs Update? | Notes |
|----------------|-----------|----------|---------------|-------|
| codebase-context.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| coding-standards.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| run-guide.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| git-workflow.md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |
| features/[X].md | Yes/No/Empty | Yes/No/NA | Yes/No | [What's wrong] |

**Workflow Friction Analysis:**

- **Stage 1 (Understand):** Did codebase-context help? What was missing?
- **Stage 2 (Analyze):** Were feature docs sufficient? What gaps?
- **Stage 4 (Modify):** Did coding-standards guide properly?
- **Stage 5 (Test):** Did run-guide have the commands needed?
- **Stage 6 (Submit):** Did git-workflow match actual process?

**Repeated Patterns:**

- **This task:** What information was searched for?
- **Previous tasks:** Have we searched for this before?
- **Pattern detected:** If yes, should we document it?

**Learning Opportunities:**

- **New pattern discovered:** [Description]
- **Should document in:** [Which file]
- **Would save time on:** [Future scenarios]

**Improvement Report Template:**

```markdown
## Skill Documentation Issues Found

### High Priority (Caused significant friction)
1. **[File]:** [What's wrong] → [Proposed fix]
2. **[File]:** [What's wrong] → [Proposed fix]

### Medium Priority (Minor delays)
1. **[File]:** [What's wrong] → [Proposed fix]

### Learning Captured
- **Pattern:** [What we learned]
- **Document in:** [Which file]
- **Benefit:** [Why this helps future tasks]

### Batch Update Recommendation
Observations: [Summary of issues across 3-5 tasks]

**Proposed batch updates:**
- Update [file-1]: [Changes]
- Update [file-2]: [Changes]
- Add [new-file]: [Purpose]

Shall I proceed with these updates?
```

**Quick Post-Task Checklist:**
- [ ] Did skill docs help or hinder?
- [ ] Any information gaps encountered?
- [ ] New patterns worth documenting?
- [ ] Conflicts between docs and reality?

**When to propose skill updates:**
- Immediately if critical gap (blocks work)
- After 3-5 tasks for minor improvements (batch updates)
- When user explicitly mentions documentation issues

---

## Retrospective Output Format

**Quick Retrospective (2 min):**

```markdown
## Task Retrospective

**What went well:**
- [Point 1]
- [Point 2]

**What could improve:**
- [Point 1]
- [Point 2]

**Action items:**
- [ ] [Action 1]
- [ ] [Action 2]
```

**Full Retrospective:**

Include all three sections above (Interaction + Code + Skill Documentation)

---

## How to Use This Guide

1. **After task completion:** Run quick retrospective
2. **Identify issues:** Note what went wrong
3. **Check skill docs:** Were they helpful or misleading?
4. **Propose updates:** If docs need improvement
5. **Track patterns:** Multiple similar issues → batch update

**The skill learns faster when:**
- Retrospectives are honest
- Patterns are identified
- Documentation is kept accurate
- Learning is captured for future tasks
