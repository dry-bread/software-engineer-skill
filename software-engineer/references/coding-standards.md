# Coding Standards

Project-specific coding conventions, style guidelines, and best practices.

---

## 🔄 Self-Improvement Guide

**When to update this file:**
- Always load this file before Stage 4 (Modify Code)
- While analyzing code to modify, observe actual patterns used
- When contradictions found between this doc and actual code

**Signals that trigger updates:**

1. **File is empty or has TODO markers**
   - Analyze existing code in files being modified
   - Document observed patterns (naming, formatting, packages)
   - Propose filling in sections with actual patterns
   
2. **Documented standard contradicts actual code**
   - While modifying code, note what's actually used vs. documented
   - Ask user: "Code uses [pattern X] but coding-standards says [pattern Y]. Should I update to reflect actual practice?"

3. **Preferred package not documented**
   - Observe consistently imported packages
   - Ask user: "I notice [package] is used throughout for [purpose]. Should I add it to preferred packages?"

4. **New pattern observed**
   - Find repeated code structures not documented
   - Ask user: "Should I document [pattern] as the standard approach for [purpose]?"

**Update proposal format:**
```
**Coding Standards Improvement**

Current state: [What's documented or missing]
Observed pattern: [What code actually does]

Proposed update to coding-standards.md:
- Section: [Which section to update]
- Change: [Specific addition/modification]
- Example: [Code example showing the pattern]

Should I update the standards?
```

**What to observe while modifying code:**
- Naming conventions (camelCase, snake_case, PascalCase)
- Indentation and spacing
- Import/require organization
- Comment styles (inline, block, docstrings)
- File structure and organization
- Error handling patterns
- Testing approaches
- Preferred packages for common tasks

---

## How to Use This File

**This file is initially empty.** It learns project standards from your code:

1. **First edit** - Analyzes existing code patterns
2. **Proposes standards** - Based on what code actually does
3. **Tracks consistency** - Detects when code deviates from documented standards

**Content will include:**
- Naming conventions (variables, functions, classes, files)
- Code formatting (indentation, line length, spacing)
- Import organization
- Comment styles
- File structure patterns
- Preferred packages and libraries
- Code organization principles
- Testing conventions

---

## Content Sections (Populated During Use)

**The skill will add these sections as needed:**

- **Language-Specific Conventions** - Style rules for each language
- **Naming Patterns** - Variable/function/class naming
- **File Organization** - How to structure files
- **Imports & Dependencies** - Preferred packages
- **Comments & Documentation** - When and how to comment
- **Error Handling** - How to handle errors
- **Testing Conventions** - Test file patterns

---

**Note:** This is a living document. It evolves as the skill learns your project's actual patterns through code observation.
