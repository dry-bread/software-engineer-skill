# Feature Documentation Index

This directory contains detailed documentation for each major feature in the application. Each feature document describes the business requirements, user flows, technical implementation, and relevant code locations.

## Purpose

Feature documentation helps:
- Understand specific feature requirements without loading entire codebase context
- Locate code related to specific functionality
- Maintain consistency when modifying features
- Onboard to feature-specific work quickly

## Organization

Features are organized by domain area:

```
features/
├── authentication/       # User authentication and authorization
├── user-management/      # User profiles and settings
├── [domain-area-1]/     # [Description]
├── [domain-area-2]/     # [Description]
└── README.md            # This file
```

## Available Features

<!-- TODO: Update this index as features are documented -->

### Authentication & Authorization

| Feature | File | Description |
|---------|------|-------------|
| User Login | [authentication/login.md](authentication/login.md) | User authentication flow, session management |
| User Registration | [authentication/registration.md](authentication/registration.md) | New user signup, validation, email verification |
| Password Reset | [authentication/password-reset.md](authentication/password-reset.md) | Password recovery and reset flow |
| OAuth Integration | [authentication/oauth.md](authentication/oauth.md) | Third-party login (Google, GitHub, etc.) |

### User Management

| Feature | File | Description |
|---------|------|-------------|
| User Profile | [user-management/profile.md](user-management/profile.md) | Profile viewing and editing |
| User Settings | [user-management/settings.md](user-management/settings.md) | Preferences, notifications, privacy settings |
| Permissions & Roles | [user-management/permissions.md](user-management/permissions.md) | Role-based access control |

### [Domain Area 1: e.g., E-commerce]

| Feature | File | Description |
|---------|------|-------------|
| [Feature 1] | [domain/feature1.md](domain/feature1.md) | [Brief description] |
| [Feature 2] | [domain/feature2.md](domain/feature2.md) | [Brief description] |

### [Domain Area 2: e.g., Analytics]

| Feature | File | Description |
|---------|------|-------------|
| [Feature 1] | [domain/feature1.md](domain/feature1.md) | [Brief description] |
| [Feature 2] | [domain/feature2.md](domain/feature2.md) | [Brief description] |

---

## Feature Document Template

Each feature document should follow this structure:

```markdown
# [Feature Name]

## Overview
[2-3 sentence description of what this feature does and why it exists]

## Business Requirements
[Key business goals and user needs this feature addresses]

## User Flows
[Step-by-step user interactions]

## Technical Implementation
[How it's built, key files, patterns used]

## API Endpoints (if applicable)
[Related endpoints]

## Database Models (if applicable)
[Related data structures]

## Dependencies
[External services, libraries, other features]

## Edge Cases & Validations
[Special cases to handle]

## Known Limitations
[Current constraints or planned improvements]

## Related Features
[Links to related feature docs]
```

---

## How to Use

### When Adding New Feature

1. Create new directory under appropriate domain area (or create new domain)
2. Create `[feature-name].md` following the template above
3. Add entry to this README index
4. Reference from main `codebase-context.md` if it's a major feature

### When Working on Existing Feature

1. Search this index for the feature name
2. Load the specific feature document
3. Use it to understand requirements and locate relevant code
4. Update the document if you discover missing information

### When User Mentions Feature

```
User: "Fix bug in password reset email"
→ Check: features/README.md for "password reset"
→ Load: features/authentication/password-reset.md
→ Work: Following feature documentation
```

---

## Maintenance Guidelines

- **Keep documents updated** - When feature changes, update its documentation
- **One feature per file** - Don't combine multiple features in one doc
- **Link related features** - Use relative links to connect related docs
- **Include code locations** - Mention key files and functions
- **Document edge cases** - Capture special behaviors and validations

---

**Note:** This is a living index. Add new features as they're developed and update existing entries as features evolve.
