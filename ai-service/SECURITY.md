1. INPUT SANITISATION
HTML tags removed
SQL injection patterns blocked (e.g., DROP TABLE)
Prompt injection detected and rejected
Returns 400 for invalid input

2. RATE LIMITING
Implemented using Flask-Limiter
Limit: 5 requests per minute per IP
Prevents brute-force and abuse

3. AUTHENTICATION (JWT)
Token-based authentication
Required for protected endpoints
Invalid/missing token → 401 response
Secret key > 32 chars for security

4. LOGGING
All requests logged in logs/app.log
Tracks warnings and suspicious activity

5. SECURITY HEADERS
X-Content-Type-Options: nosniff
X-Frame-Options: DENY

6. OWASP ZAP TESTING
Performed baseline scan
No critical vulnerabilities found
Medium/Low risks mitigated

7. THREATS MITIGATED
SQL Injection
XSS (via sanitisation)
Brute force (rate limiting)
Unauthorized access (JWT)
Prompt injection

8. CONCLUSION
All major OWASP Top 10 risks addressed.
System is secure for MVP usage.