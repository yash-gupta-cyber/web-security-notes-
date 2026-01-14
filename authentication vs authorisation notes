# Authentication vs Authorization

## Overview
Authentication and authorization are two core security concepts used by web applications to control user access. Although they are closely related, they serve different purposes and are often confused.

Understanding the difference between them is critical for identifying access control vulnerabilities.

---

## What is Authentication?
Authentication is the process of verifying **who a user is**.

It answers the question:
> “Are you really who you claim to be?”

Common authentication methods include:
- Username and password
- One-time passwords (OTP)
- Multi-factor authentication (MFA)
- Session-based authentication
- Token-based authentication

If authentication fails, the user should not be logged in.

---

## What is Authorization?
Authorization determines **what an authenticated user is allowed to do**.

It answers the question:
> “What actions are you allowed to perform?”

Examples:
- Can the user access an admin page?
- Can the user edit or delete a resource?
- Can the user view another user’s data?

Authorization is checked **after authentication**.

---

## Key Differences

| Authentication | Authorization |
|----------------|--------------|
| Verifies identity | Controls permissions |
| Happens first | Happens after authentication |
| Uses credentials | Uses roles, rules, or policies |
| Example: Login | Example: Access control |

Both must be implemented correctly to ensure application security.

---

## Common Security Issues

### Authentication Issues
- Weak passwords
- Missing rate limiting
- Credential reuse
- Poor session handling

### Authorization Issues
- Broken access control
- Insecure direct object references (IDOR)
- Missing role checks
- Client-side authorization logic

Many serious vulnerabilities occur when authorization checks are missing or improperly enforced.

---

## Real-World Example
A user successfully logs in to an application (authentication succeeds).

However, by changing a URL parameter or request ID, the user can access another user’s data.

This is an **authorization failure**, not an authentication issue.

---

## Why This Matters for Web Security
Authorization vulnerabilities are among the most common and impactful issues reported in bug bounty programs. They often lead to:
- Data exposure
- Account takeover scenarios
- Privilege escalation

Clear understanding of this distinction helps in identifying and reporting issues accurately.

---

## Conclusion
Authentication confirms identity, while authorization defines access. Both are essential for secure web applications, and weaknesses in either can result in serious security vulnerabilities.
