# Run Guide

How to run, test, and debug this project.

---

## 1. Running the Project

#

## When Run Guide is Empty

**If sections above are empty or incomplete:**

```
WORKFLOW:
1. Check for project documentation
   a. Read README.md or README.rst
   b. Look for CONTRIBUTING.md, docs/ folder
   c. Check package.json "scripts", Makefile, docker-compose.yml
   
2. If documentation found:
   → Extract run instructions
   → Organize into sections above (Prerequisites, Setup, Running, etc.)
   → Ask user: "Found run instructions in [source]. Should I populate run-guide with:
      - Prerequisites: [list]
      - Setup: [steps]
      - Run command: [command]
      ?"

3. If no documentation found:
   a. Analyze project structure to infer:
      - Language/framework (package.json → Node.js, requirements.txt → Python, etc.)
      - Likely commands (npm start, python main.py, mvn run, etc.)
   
   b. Ask user:
      "No run documentation found. Based on project structure:
      - Detected: [language/framework]
      - Typical commands: [inferred commands]
      
      Do you have run documentation? Or should I try these commands?"

4. After first successful run:
   → Document all steps that were actually needed
   → Populate relevant sections above
   → Create troubleshooting entries for any issues encountered
```

---

##  During Code Execution

**While running code, monitor for process gaps:**

```
WORKFLOW:
1. Execute run command from Step 4

2. If error occurs, classify:
   
   ✅ PROCESS GAP (document in run-guide):
   - "Module not found" → Missing dependency installation step
   - "Port already in use" → Add to troubleshooting
   - "Environment variable X not set" → Add to Step 3
   - "Database connection failed" → Missing setup step
   - "Permission denied" → Missing prerequisite or setup
   
   ❌ CODE ISSUE (fix code, don't document as process):
   - "Null pointer exception" → Code bug
   - "Invalid API response" → Code logic error
   - "Validation failed" → Code implementation issue
   - "Type error" → Code syntax/type problem

3. If user provides missing instruction:
   
   Track repetition:
   - First time: Note it
   - Second time: Process gap detected
   - Ask user: "You've provided '[instruction]' twice. This seems like a setup step 
     missing from run-guide. Should I add it to [Section]?"

4. After successful run:
   
   Verify documentation:
   - Did documented steps match actual needs?
   - Were any steps missing?
   - Were any steps unclear?
   - Did troubleshooting section help?
   
   If gaps found:
   → Propose update with specific improvements

5. Update sections above:
   - Add missing prerequisites
   - Clarify unclear steps
   - Add new troubleshooting entries
   - Document environment variables
```
