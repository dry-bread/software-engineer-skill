# Coding Standards

Project-specific coding conventions and style guidelines.

---

## Workflow: Following Coding Standards

### Current Coding Standards

**Naming Conventions:**

*This section will be populated after analyzing project code.*

**Code Formatting:**

*This section will be populated after analyzing project code.*

**Import Organization:**

*This section will be populated after analyzing project code.*

**Comment Styles:**

*This section will be populated after analyzing project code.*

**File Structure:**

*This section will be populated after analyzing project code.*

**Preferred Packages:**

*This section will be populated after analyzing project code.*

**Error Handling:**

*This section will be populated after analyzing project code.*

**Testing Conventions:**

*This section will be populated after analyzing project code.*

---

## Workflow: When Coding Standards are Empty

**If sections above are empty:**

```
WORKFLOW:
1. Before modifying code, analyze existing code files
   
   a. Read files you're about to modify
   b. Read similar files in the same module
   c. Observe patterns:
      - Naming: camelCase? snake_case? PascalCase?
      - Indentation: 2 spaces? 4 spaces? Tabs?
      - Imports: How are they organized? Any consistent order?
      - Comments: Inline? Block? Docstrings? JSDoc?
      - File structure: Imports → Constants → Functions → Exports?
      - Error handling: try/catch? if/else? Custom errors?
      - Testing: Co-located tests? Separate test folder?

2. Document observed patterns
   
   Propose to user:
   "No coding standards documented yet. Based on analyzing [files]:
   
   Observed patterns:
   - Naming: Variables use [pattern], Functions use [pattern]
   - Formatting: [X] spaces indentation, [Y] line length
   - Imports: [Organization pattern]
   - Comments: [Style observed]
   - Packages: Consistently using [package] for [purpose]
   
   Should I populate coding-standards.md with these patterns?"

3. After first code modification:
   
   - Document all patterns followed
   - Populate relevant sections above
   - Create initial coding standards baseline
```

---

## Workflow: During Code Modification

**While modifying code, maintain consistency:**

```
WORKFLOW:
1. Load current coding standards (sections above)

2. Follow documented patterns
   - Use documented naming conventions
   - Match documented formatting
   - Organize imports as documented
   - Follow documented file structure

3. Observe existing code being modified
   
   Check consistency:
   a. Does existing code follow documented standards?
   b. If YES → Follow the same patterns
   c. If NO → Detected inconsistency
   
   When inconsistency found:
   - OPTION A: Code is correct, docs are wrong
     → Ask: "Code uses [X] but docs say [Y]. Should I update docs?"
   
   - OPTION B: Code is outdated, docs are correct
     → Follow docs, refactor code to match standards

4. Discover new patterns not documented
   
   If you notice:
   - Consistently used package not in "Preferred Packages"
   - Repeated code structure not documented
   - Common error handling pattern not captured
   
   → Ask: "Found [pattern] used throughout. Should I add to standards?"

5. Write new code following standards
   
   - Apply documented naming conventions
   - Match documented formatting
   - Use documented patterns
   - Follow documented structure
```
