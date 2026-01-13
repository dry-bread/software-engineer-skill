# Software Engineer Skill

A self-evolving Copilot skill that provides standardized workflows for software engineering tasks: understanding requirements, analyzing code, modifying implementation, running tests, and submitting changes.

## Overview

This skill turns chaotic code editing into a structured 6-stage workflow. It learns from your codebase automatically, documenting patterns, conventions, and processes as you work.

**Key Innovation:** Self-learning reference files that evolve with your project. Empty at start, they populate themselves by observing your code, run commands, git workflows, and team practices.

## Core Features

### ✅ Structured 6-Stage Workflow
1. **Understand Requirements** - Parse requests, clarify ambiguities
2. **Analyze Code** - Locate files, understand implementation
3. **Propose Solution** - Design approach, get user approval
4. **Modify Code** - Implement following project standards
5. **Run & Test** - Verify changes work as expected
6. **Submit & Summarize** - Create branch, commit, generate PR

### 🧠 Self-Learning Documentation
- **Coding Standards** - Learns naming conventions, formatting, preferred packages from actual code
- **Run Guide** - Captures setup steps, run commands, troubleshooting from real attempts
- **Git Workflow** - Observes branch naming, commit formats, PR process from repository
- **Codebase Context** - Documents business logic, features, architecture as you work
- **Retrospectives** - Analyzes what worked/failed, proposes skill improvements

### 📚 Progressive Disclosure
- Only loads relevant documentation when needed
- Feature-specific docs organized separately (avoid loading entire codebase)
- Token-efficient design for large projects

### 🔄 Continuous Improvement
- Reference files detect their own gaps
- Propose updates when documented patterns contradict reality
- Track repeated user instructions and suggest documenting them
- Distinguish process gaps (document) from code bugs (fix code)

## Repository Structure

```
software-engineer-skill/
├── README.md                          # This file
└── software-engineer/
    ├── SKILL.md                       # Main skill definition (6-stage workflow)
    └── references/
        ├── codebase-context.md        # Project overview, business logic, feature index
        ├── coding-standards.md        # Naming, formatting, patterns (learns from code)
        ├── run-guide.md               # Setup, run commands, troubleshooting (learns from runs)
        ├── git-workflow.md            # Branch naming, commits, PRs (learns from git)
        ├── retrospective-guide.md     # Post-task analysis framework
        └── features/
            ├── README.md              # Feature index
            ├── TEMPLATE.md            # Template for new feature docs
            └── [domain]/
                └── [feature].md       # Detailed feature documentation
```

## How It Works

### Initial State: Empty Documentation

All reference files start empty or with minimal templates. This is intentional.

### Learning Through Work

As you use the skill to work on code:

1. **First code edit** → Skill analyzes existing code patterns, proposes documenting them in `coding-standards.md`
2. **First run attempt** → Skill reads README/package.json, proposes documenting steps in `run-guide.md`
3. **First PR** → Skill observes git history, proposes documenting conventions in `git-workflow.md`
4. **User mentions feature** → Skill searches code, proposes creating `features/[domain]/[feature].md`

### Self-Improvement Triggers

Each reference file monitors for:
- **Empty sections** → Analyze project, propose initial content
- **Documentation contradicts reality** → Propose updating docs
- **User repeatedly provides same info** → Propose documenting it
- **New patterns discovered** → Propose adding to standards

### Example Learning Cycle

```
Task: "Add password validation to registration"

Stage 1: Load codebase-context.md
→ Empty, no feature docs
→ Skill searches code, finds registration logic
→ Proposes: "Create features/authentication/registration.md?"

Stage 4: Modify code
→ coding-standards.md is empty
→ Skill analyzes existing code: camelCase, 2-space indent, etc.
→ Proposes: "Document observed patterns as coding standards?"

Stage 5: Run tests
→ run-guide.md is empty
→ User says "run npm test"
→ Skill proposes: "Add 'npm test' to run-guide.md?"

Stage 6: Submit PR
→ User creates branch "feature/password-validation"
→ git-workflow.md is empty
→ Skill proposes: "Document 'feature/' branch prefix as convention?"

Next task: Similar changes require no questions - skill follows documented patterns.
```

## Workflow Details

### Stage 1: Understand Requirements
- Parse user request (feature/bug/investigation/refactor)
- Clarify ambiguities
- Load `codebase-context.md` for project context

### Stage 2: Analyze Code
- Locate relevant files (semantic/file search)
- Load specific feature docs from `features/` if mentioned
- Trace dependencies and impact scope

### Stage 3: Propose Solution
- Design approach (clarity, consistency, minimal impact)
- Present plan to user
- Get approval before proceeding

### Stage 4: Modify Code
- **Load `coding-standards.md`** before writing code
- Follow documented conventions
- Detect and propose updates if standards contradict code

### Stage 5: Run & Test
- **Load `run-guide.md`**
- Execute according to documented steps
- Classify errors: process gap (document) vs code bug (fix)
- Propose updates when steps are missing

### Stage 6: Submit & Summarize
- **Load `git-workflow.md`**
- Follow documented branch/commit/PR conventions
- Generate comprehensive change summary
- Observe user corrections and propose standardizing them

## Usage

### Quick Start

1. Copy this skill to your Copilot skills directory
2. Trigger with requests like:
   - "Add feature X"
   - "Fix bug Y"
   - "Run the project"
   - "Investigate issue Z"

3. First time: Reference files are empty
   - Skill will analyze your project
   - Propose documenting patterns
   - Accept or customize proposals

4. Subsequent times: Skill follows learned patterns
   - Automatically applies coding standards
   - Uses documented run commands
   - Follows git conventions

### Trigger Patterns

The skill activates when you ask to:
- Add features, fix bugs, refactor code
- Run projects, debug errors
- Understand business logic, investigate issues
- Submit PRs, review changes
- Conduct retrospectives

### Customization

Reference files are markdown - edit them directly:
- Add project-specific business context
- Document team-specific conventions
- Customize workflow stages
- Add new feature documentation

## Benefits

### For Individual Developers
- **Consistency** - Always follow project conventions
- **Less context switching** - Documentation loads when needed
- **Faster onboarding** - Skill learns and documents project for you

### For Teams
- **Standardization** - Everyone follows same workflow
- **Living documentation** - Stays in sync with reality
- **Knowledge capture** - Patterns documented automatically

### For Projects
- **Self-documenting** - Code patterns become explicit
- **Maintainability** - New contributors understand conventions
- **Evolution** - Documentation adapts as project changes

## Advanced Features

### Feature Documentation System

Organize detailed feature docs separately:

```
references/features/
├── authentication/
│   ├── login.md           # User flows, API endpoints, security
│   ├── registration.md    # Validation rules, email flow
│   └── oauth.md           # Provider setup, callback handling
├── payments/
│   └── checkout.md        # Payment flow, error handling
└── README.md              # Index of all features
```

Load only when feature is mentioned → Token-efficient for large codebases.

### Retrospective Analysis

After each task, analyze:
1. **Interaction quality** - How efficient was the conversation?
2. **Code quality** - Is the solution optimal?
3. **Skill effectiveness** - Did documentation help or hinder?

Identify patterns, propose batch updates to improve skill over time.

### Process vs Code Distinction

Smart classification of issues:
- ✅ **Process gap** → Document in run-guide
  - Missing env var setup
  - Undocumented prerequisite
  - Unclear run command
  
- ❌ **Code bug** → Fix code, don't document
  - Null pointer exception
  - Logic error
  - API validation failure

## Philosophy

**Documentation comes from reality, not assumptions.**

- Standards are discovered by observing code
- Run steps are captured from actual attempts  
- Git conventions are inferred from repository
- Features are documented as they're worked on

**The skill should disappear into the workflow.**

- No upfront configuration required
- Learns by watching you work
- Proposes updates, never forces them
- Adapts to your project, not vice versa

## Contributing

To improve this skill:

1. Use it on real projects
2. Note what works and what doesn't
3. Propose improvements via retrospectives
4. Share learnings in issues/PRs

## License

MIT License - Use freely, modify as needed, share improvements.

## Credits

Created for GitHub Copilot's skill system. Designed to reduce cognitive load and increase code quality through structured workflows and self-learning documentation.
