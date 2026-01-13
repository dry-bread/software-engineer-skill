# Run Guide

Instructions for running, testing, and debugging this project.

---

## 🔄 Self-Improvement Guide

**When to update this file:**
- Load this file at Stage 5 (Run & Test)
- When setup fails or requires manual intervention
- When user repeatedly provides run instructions

**Signals that trigger updates:**

1. **File is empty or incomplete**
   - Read project README for run instructions
   - Check package.json scripts, Makefile, docker-compose.yml
   - Ask user: "Run guide is incomplete. Should I initialize it based on [what I found]? Or do you have docs I should reference?"

2. **User repeatedly provides same run instructions**
   - Track if user says same thing multiple times
   - Distinguish code issues (ignore) from process gaps (important)
   - Ask user: "[Specific instruction] was needed but not in run-guide. Should I add it?"

3. **Runtime errors due to missing setup**
   - Note errors caused by missing env vars, dependencies, or setup steps
   - Ask user: "Error '[X]' suggests missing [Y]. Should I add this to troubleshooting?"

4. **Success pattern not documented**
   - If run succeeds but steps weren't fully documented
   - Capture the successful workflow

**Update proposal format:**
```
**Run Guide Improvement**

Gap identified: [What caused friction]
User action required: [What user had to provide/fix]

Proposed update to run-guide.md:
- Section: [Prerequisites/Setup/Running/Troubleshooting]
- Addition: [Specific content to add]

This is a process gap, not a code issue. Should I document it?
```

**Distinguish process vs. code issues:**
- ✅ **Process gap** (document it):
  - Missing environment variable in .env example
  - Undocumented prerequisite software
  - Missing database migration step
  - Unclear run command
- ❌ **Code issue** (fix the code, don't document as process):
  - Logic bug causing runtime error
  - Incorrect API endpoint
  - Missing error handling

**Key principle:** If the solution is to change code, it's a code issue. If the solution is for the developer to do something (install, configure, run a command), it's a process gap that belongs here.

---

## How to Use This File

**This file is initially empty.** It learns from your project setup:

1. **First run attempt** - Discovers how to run the project
2. **Captures setup** - Documents prerequisites and environment
3. **Tracks gaps** - When you provide missing setup steps, proposes documenting them

**Content will include:**
- Prerequisites (languages, tools, services)
- Initial setup steps
- Environment configuration
- How to run (dev, test, build, deploy)
- Debugging techniques
- Troubleshooting common issues

---

## Content Sections (Populated During Use)

**The skill will add these sections as needed:**

- **Prerequisites** - Required software and versions
- **Initial Setup** - First-time installation steps
- **Environment Variables** - Required configuration
- **Running the Application** - Dev/test/prod commands
- **Testing** - How to run tests
- **Debugging** - Common debugging approaches
- **Troubleshooting** - Known issues and solutions

---

**Note:** This is a living document. It evolves through actual run attempts and captures real setup requirements.
