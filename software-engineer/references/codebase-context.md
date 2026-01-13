# Codebase Context

Project-specific context: business domain, architecture, and feature documentation index.

---

## Workflow: Understanding Project Context

### Step 1: Check Available Features

**Current features documented in this project:**

| Feature Area | Key Features | Documentation Path |
|--------------|--------------|-------------------|
| **Authentication** | Login, Registration, OAuth | [features/authentication/](features/authentication/) |
| **User Management** | Profiles, Permissions, Settings | [features/user-management/](features/user-management/) |

*Note: This list will grow as more features are documented.*

---

### Step 2: Load Specific Feature Documentation

**When user mentions a feature:**

1. **Check if feature is listed above**
   - If yes → Load the specific feature documentation file
   - If no → Proceed to Step 3

2. **Load and read feature documentation**
   - Example: User asks about "login" → Load `features/authentication/login.md`
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

---

### Step 4: Load Project Overview (When Needed)

**This file can also contain:**
- **Project Overview** - Purpose, tech stack, key features
- **Repository Structure** - Directory organization
- **Architecture Patterns** - Design patterns used
- **Data Models** - Key entities and relationships
- **Common Scenarios** - Typical development patterns

**These sections are populated as you work on the project.**

---

## When to Use This File

Load during:
- **Stage 1 (Understand Requirements)** - Get business context
- **Stage 2 (Analyze Code)** - Understand feature architecture
- When user mentions specific features or business logic
- When investigating unfamiliar parts of codebase

---

## Feature Documentation Organization

```
references/features/
├── authentication/
│   ├── login.md
│   ├── registration.md
│   └── password-reset.md
├── user-management/
│   ├── profile.md
│   ├── permissions.md
│   └── settings.md
├── [domain-area]/
│   └── [feature].md
└── README.md  # Feature index with all features
```

---

## 🔄 Self-Improvement Workflow

**When to update this file:**
- When loaded during Stage 1 or Stage 2
- When feature documentation is missing or outdated
- When user mentions features not in the feature table

**Update triggers:**

1. **Feature table is empty or incomplete**
   - After analyzing code and finding undocumented features
   - After creating new feature documentation
   - Add entry to Step 1 feature table

2. **Feature documentation contradicts code**
   - Discovered during Step 2 verification workflow
   - Update feature doc, not this file (this file only indexes features)

3. **Project overview sections needed**
   - If file lacks tech stack, architecture info
   - Read README, package.json, analyze structure
   - Propose adding sections to Step 4

**Update proposal format:**
```
**Codebase Context Update**

Action: [Add feature to table / Add project overview section]
Found: [What was discovered in code]

Proposed update:
- Add to feature table: [Feature name, domain, file path]
- OR Add section: [Project Overview / Architecture / Data Models]

Should I proceed?
```
