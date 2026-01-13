# Codebase Context

Project-specific context: business domain, architecture, and feature documentation index.

---

## Workflow: Understanding Project Context

### Step 1: Check Available Features

**Current features documented in this project:**

| Feature Area | Key Features | Documentation Path |
|--------------|--------------|-------------------|
| |  | |
| | |  |

*Note: This list will grow as more features are documented.*

---

### Step 2: Load Specific Feature Documentation

**When user mentions a feature:**

1. **Check if feature is listed above**
   - If yes → Load the specific feature documentation file
   - If no → Proceed to Step 3

2. **Load and read feature documentation**
   - Get business requirements, user flows, technical details

3. **After reading feature docs, verify against code:**
   ```
   WORKFLOW:
   a. Locate relevant code files mentioned in feature doc
   b. Read actual implementation
   c. Compare documentation vs. reality
   d. If mismatch found:
      → Ask user: "Feature doc says [X] but code does [Y]. Should I update the docs?"
   e. If code has new logic not documented:
      → Ask user: "Found [new behavior] in code. Should I add this to feature doc?"
   ```

---

### Step 3: Feature Not Documented Yet

**If feature is NOT in the list above:**

```
WORKFLOW:
1. Search codebase for feature-related files
   - Use semantic search with feature name
   - Look for controllers, services, components, etc.

2. Read and analyze the code
   - Identify entry points (API endpoints, UI components)
   - Trace business logic flow
   - Note dependencies and data models

3. Draft feature documentation
   - Use features/TEMPLATE.md as structure
   - Document: Overview, Business Requirements, User Flows, 
     Technical Implementation, API Endpoints, Edge Cases

4. Propose to user:
   "Feature [X] isn't documented yet. Based on code analysis:
   - Found in: [file paths]
   - Purpose: [what it does]
   - Key logic: [main flows]
   
   Should I create features/[domain]/[feature-name].md with this info?"

5. If user approves:
   - Create feature documentation file
   - Add to this file's feature table (Step 1)
```


