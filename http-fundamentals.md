# HTTP Fundamentals

## What is HTTP?
HTTP (Hypertext Transfer Protocol) is the protocol used for communication between a client (usually a web browser) and a server. It defines how requests are sent and how responses are returned over the web.

HTTP works on a request–response model, where the client initiates a request and the server responds with data.

---

## Client and Server
- **Client**: A browser, mobile app, or tool (e.g., curl, Burp Suite) that sends requests.
- **Server**: A system that receives requests and sends responses.

Understanding this interaction is essential for identifying web vulnerabilities.

---

## HTTP Requests
An HTTP request is sent by the client to ask the server to perform an action.

### Common Request Methods
- **GET** – Retrieve data from the server
- **POST** – Send data to the server
- **PUT** – Update existing data
- **DELETE** – Remove data
- **OPTIONS** – Check allowed methods

Each method has different security implications.

---

## HTTP Responses
After receiving a request, the server returns an HTTP response.

### Common Status Codes
- **200 OK** – Request successful
- **301 / 302** – Redirect
- **400 Bad Request** – Invalid client request
- **401 Unauthorized** – Authentication required
- **403 Forbidden** – Access denied
- **404 Not Found** – Resource not found
- **500 Internal Server Error** – Server error

Status codes help understand how the server handled the request.

---

## HTTP Headers
Headers contain additional information about the request or response.

### Common Request Headers
- `Host`
- `User-Agent`
- `Cookie`
- `Authorization`
- `Content-Type`

### Common Response Headers
- `Set-Cookie`
- `Content-Type`
- `Content-Length`
- `Location`

Many security issues arise due to improper handling of headers.

---

## Cookies and Sessions
Cookies are small pieces of data stored in the browser and sent with each request.

They are commonly used for:
- Session management
- Authentication
- User tracking

Poor cookie configuration can lead to vulnerabilities such as session hijacking.

---

## HTTP vs HTTPS
- **HTTP**: Data is sent in plain text
- **HTTPS**: Data is encrypted using TLS

HTTPS protects data from being intercepted or modified by attackers.

---

## Why HTTP is Important for Security
Most web vulnerabilities occur because of:
- Improper request validation
- Broken authentication
- Incorrect access control
- Insecure session handling

Understanding HTTP is the foundation of web application security.

---

## Conclusion
A strong understanding of HTTP fundamentals helps in identifying, reproducing, and reporting web vulnerabilities accurately. It is one of the most important skills for anyone learning web security or bug bounty.
