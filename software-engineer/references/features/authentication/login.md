# User Login

## Overview

User authentication feature that allows registered users to access the application using their credentials. Supports email/password login and optional remember-me functionality.

## Business Requirements

**Primary Goals:**
- Secure user authentication
- Session management
- Failed login attempt tracking
- Account lockout after multiple failed attempts

**User Stories:**
- As a user, I want to log in with my email and password
- As a user, I want to stay logged in across browser sessions
- As a user, I want to be notified if my credentials are incorrect
- As a system, I want to prevent brute force attacks

## User Flows

### Successful Login Flow

1. User navigates to login page
2. User enters email and password
3. (Optional) User checks "Remember me" checkbox
4. User clicks "Login" button
5. System validates credentials
6. System creates session
7. User is redirected to dashboard/home page

### Failed Login Flow

1. User enters invalid credentials
2. System increments failed attempt counter
3. System displays error message
4. If attempts < 5: User can retry
5. If attempts >= 5: Account locked for 15 minutes

### Remember Me Flow

1. User checks "Remember me" during login
2. System issues long-lived token (30 days)
3. User can close browser and return
4. System validates token and auto-logs in user

## Technical Implementation

### Key Files

<!-- TODO: Add actual file paths from your project -->

```
[path/to/auth/controller.js]    # Login endpoint handler
[path/to/auth/service.js]        # Authentication logic
[path/to/user/model.js]          # User model with password methods
[path/to/session/manager.js]     # Session creation and validation
[path/to/auth/middleware.js]     # Authentication middleware
```

### Code Locations

**Login Handler:**
```
File: [path/to/auth/controller.js]
Function: handleLogin()
Lines: [X-Y]
```

**Password Validation:**
```
File: [path/to/user/model.js]
Function: validatePassword()
Lines: [X-Y]
```

**Session Creation:**
```
File: [path/to/session/manager.js]
Function: createSession()
Lines: [X-Y]
```

## API Endpoints

### POST /api/auth/login

**Request:**
```json
{
  "email": "user@example.com",
  "password": "securePassword123",
  "rememberMe": true
}
```

**Success Response (200):**
```json
{
  "success": true,
  "user": {
    "id": "123",
    "email": "user@example.com",
    "name": "John Doe"
  },
  "token": "jwt-token-here",
  "expiresIn": 86400
}
```

**Error Response (401):**
```json
{
  "success": false,
  "error": "Invalid email or password",
  "attemptsRemaining": 3
}
```

**Account Locked Response (423):**
```json
{
  "success": false,
  "error": "Account locked due to multiple failed attempts",
  "lockoutEndsAt": "2026-01-13T15:30:00Z"
}
```

## Database Models

### User Model

<!-- TODO: Update with actual schema -->

```javascript
{
  id: String,
  email: String (unique, indexed),
  passwordHash: String,
  failedLoginAttempts: Number (default: 0),
  lockedUntil: Date (nullable),
  lastLoginAt: Date,
  createdAt: Date,
  updatedAt: Date
}
```

### Session Model

```javascript
{
  id: String,
  userId: String (foreign key),
  token: String (indexed),
  expiresAt: Date,
  rememberMe: Boolean,
  ipAddress: String,
  userAgent: String,
  createdAt: Date
}
```

## Dependencies

**External Services:**
- None (fully internal authentication)

**Libraries:**
- `bcrypt` - Password hashing and comparison
- `jsonwebtoken` - JWT token generation
- `express-session` - Session middleware

**Related Features:**
- [User Registration](registration.md) - Creating new accounts
- [Password Reset](password-reset.md) - Recovering access
- [User Profile](../user-management/profile.md) - Post-login user data

## Security Considerations

### Password Handling
- Passwords are hashed using bcrypt with cost factor 12
- Never log or expose passwords in any form
- Use constant-time comparison for password validation

### Brute Force Protection
- Maximum 5 failed attempts per 15-minute window
- Account locked for 15 minutes after 5 failures
- Consider implementing CAPTCHA after 3 failures (future enhancement)

### Session Security
- Tokens stored as HTTP-only cookies
- CSRF protection enabled
- Token rotation on each request (if using refresh tokens)
- Invalidate all sessions on password change

### Rate Limiting
<!-- TODO: Add rate limiting configuration -->
- Limit: [X requests per minute] per IP address
- Implemented in: [middleware/file.js]

## Edge Cases & Validations

### Input Validation

**Email:**
- Required field
- Must be valid email format
- Case-insensitive matching
- Trimmed of whitespace

**Password:**
- Required field
- Minimum length: [8] characters
- No maximum length limit on login (only on registration)
- Exact match required (case-sensitive)

### Edge Cases

1. **User doesn't exist:**
   - Show same error as wrong password (prevent email enumeration)
   - Don't increment failed login counter

2. **Account already locked:**
   - Check lockout expiry
   - Auto-unlock if time passed
   - Show remaining lock time

3. **Concurrent login attempts:**
   - Use database transactions for failed attempt counter
   - Prevent race conditions

4. **Password recently changed:**
   - Invalidate old sessions
   - Require new login

5. **Session expired:**
   - Return 401 Unauthorized
   - Redirect to login page
   - Preserve intended destination URL

## Known Limitations

<!-- TODO: Document current limitations -->

1. **Single device sessions:**
   - Currently no limit on concurrent sessions
   - Consider adding session management UI (future)

2. **No 2FA:**
   - Two-factor authentication not yet implemented
   - Planned for future release

3. **IP-based rate limiting:**
   - May affect users behind shared IPs (NAT)
   - Consider moving to email-based rate limiting

## Performance Considerations

- Login endpoint response time target: < 200ms
- Password hashing is CPU-intensive (bcrypt cost 12)
- Session lookups are indexed by token
- Consider caching user data after successful login

## Testing

### Test Coverage

<!-- TODO: Add test file locations -->

**Unit Tests:**
- `[tests/auth/login.test.js]` - Login logic tests
- `[tests/auth/password.test.js]` - Password validation tests

**Integration Tests:**
- `[tests/integration/auth-flow.test.js]` - End-to-end login flow

**Test Scenarios:**
- ✅ Successful login with valid credentials
- ✅ Failed login with wrong password
- ✅ Failed login with non-existent email
- ✅ Account lockout after 5 failed attempts
- ✅ Remember me functionality
- ✅ Session expiration
- ✅ Concurrent login handling

## Related Features

- **[User Registration](registration.md)** - How users create accounts
- **[Password Reset](password-reset.md)** - Password recovery flow
- **[User Profile](../user-management/profile.md)** - Post-login user management
- **[Permissions](../user-management/permissions.md)** - Authorization after authentication

## Troubleshooting

### Common Issues

**Issue: User can't log in after password reset**
- Check: Password hash was updated correctly
- Check: Old sessions were invalidated
- Check: No account lockout is active

**Issue: "Remember me" not working**
- Check: Cookie settings (HTTP-only, Secure, SameSite)
- Check: Token expiration time
- Check: Browser cookie storage enabled

**Issue: Account locked unexpectedly**
- Check: Failed attempt counter
- Check: Lockout timestamp
- Manual unlock: Reset `failedLoginAttempts` to 0 and clear `lockedUntil`

---

**Last Updated:** [Date]
**Maintained By:** [Team/Person]
