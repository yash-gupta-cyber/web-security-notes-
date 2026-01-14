# Cookies and Sessions

## Overview
Cookies and sessions are fundamental mechanisms used by web applications to maintain state and manage user authentication. Since HTTP is stateless by default, these mechanisms allow applications to recognize users across multiple requests.

A solid understanding of cookies and sessions is essential for identifying many common web security vulnerabilities.

---

## What Are Cookies?
Cookies are small pieces of data stored in the user's browser and automatically sent with each HTTP request to the same domain.

They are commonly used for:
- Session identification
- User preferences
- Authentication tokens
- Tracking and analytics

Cookies are created by the server using the `Set-Cookie` response header.

---

## Important Cookie Attributes
Cookie attributes control how and when cookies are sent by the browser.

- **Secure**  
  Ensures the cookie is only sent over HTTPS connections.

- **HttpOnly**  
  Prevents JavaScript from accessing the cookie, reducing the risk of client-side attacks.

- **SameSite**  
  Controls whether cookies are sent with cross-site requests.
  - `Strict`
  - `Lax`
  - `None`

Improper cookie attributes can lead to serious security issues.

---

## What Are Sessions?
A session is a server-side mechanism used to store user-related data. Instead of storing sensitive information in the browser, the server stores it and associates it with a unique session identifier.

The session identifier is usually stored in a cookie on the client side.

---

## How Sessions Work
1. User logs in
2. Server creates a session and generates a session ID
3. Session ID is sent to the browser as a cookie
4. Browser sends the session ID with every request
5. Server uses the session ID to identify the user

If an attacker obtains the session ID, they may be able to impersonate the user.

---

## Common Security Issues
Poor handling of cookies and sessions can lead to vulnerabilities such as:
- Session hijacking
- Session fixation
- Cross-site scripting (XSS) impact
- Cross-site request forgery (CSRF)

Many real-world attacks exploit weak session management rather than complex bugs.

---

## Best Practices
- Always use HTTPS
- Set `HttpOnly` and `Secure` flags on sensitive cookies
- Use appropriate `SameSite` values
- Regenerate session IDs after login
- Invalidate sessions on logout

---

## Why This Matters for Bug Bounty
A large number of accepted bug bounty reports involve:
- Missing cookie flags
- Insecure session handling
- Authentication logic flaws

Understanding cookies and sessions helps in identifying these issues early and reporting them clearly.

---

## Conclusion
Cookies and sessions are a core part of web application security. Misconfigurations can lead to serious vulnerabilities, making this topic critical for anyone learning web security or responsible vulnerability research.
