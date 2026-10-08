\# Security Assessment Report



\## Finding 1 — Weak Password Recovery Mechanism



\*\*Severity:\*\* High



\*\*Affected Component:\*\* Forgot Password / Account Recovery



\### Description



The application uses a security question as part of its password recovery process. In the intentionally vulnerable OWASP Juice Shop laboratory environment, the answer can be determined from publicly available information.



\### Impact



An attacker who discovers the answer may be able to reset the user's password, resulting in potential unauthorized account access.



\### Evidence



The issue was successfully reproduced in the authorized local OWASP Juice Shop lab.



Evidence:



`../evidence/reset-jims-password.png`



\### Recommended Mitigation



1\. Avoid security questions with publicly discoverable answers.

2\. Use cryptographically random password-reset tokens.

3\. Make reset tokens single-use and short-lived.

4\. Deliver recovery links through verified channels.

5\. Consider multi-factor authentication for account recovery.



\### Testing Environment



\- OWASP Juice Shop

\- Docker

\- Localhost

\- `http://localhost:3000`



Testing was performed only against the authorized local training environment.

