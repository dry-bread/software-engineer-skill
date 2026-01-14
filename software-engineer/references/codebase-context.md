# Codebase Context
This document provides an overview of the project's business domains, architecture, and feature documentation index.

**Purpose:**
- Provide a high-level summary of business logic and design
- Document key functional areas and considerations
- Index detailed feature documentation (features/)
- Does not include specific coding standards and technical details (refer to coding-standards.md)


## Background

### Project Overview

**Trident Data Engineering and Data Science Extension** is the codebase for Microsoft Fabric's data engineering and data science capabilities. This monorepo contains the web-based extensions that power notebook experiences, Spark job management, language services, and data visualization features in the Fabric platform.

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
      → update the docs align to actual code logic
   ```

---

### Step 3: Feature Not Documented Yet

**If feature is NOT in the list above:**

```
WORKFLOW:
1. Search codebase for feature-related files
2. Read and analyze the code
   - Identify entry points (API endpoints, UI components)
   - Trace business logic flow
   - Note dependencies and data models

3. Draft feature documentation
   - add a new file under ./features
   - Document: Overview, Business Requirements, User Flows,
     Technical Implementation, API Endpoints, Edge Cases
```


