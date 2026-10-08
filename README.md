\# SWYNEX Security Fundamentals Assessment



Security assessment completed as part of the SWYNEX internship.



\## Objective



Perform a security assessment in an authorized lab environment and document security risks, affected components, evidence, and recommended mitigations.



\## Lab Environment



\- Application: OWASP Juice Shop

\- Environment: Local Docker container

\- Target: http://localhost:3000

\- Testing scope: Authorized local training environment



\## Finding 1: Weak Password Recovery Mechanism



\### Affected Component



Forgot Password / Account Recovery.



\### Description



The password recovery process uses a security question whose answer can be discovered from publicly available information.



\### Risk



An attacker who determines the answer may be able to reset a user's password and potentially gain unauthorized access to the account.



\### Evidence



The vulnerability was successfully reproduced in the authorized local OWASP Juice Shop lab.



See:



`evidence/reset-jims-password.png`



\### Recommended Mitigation



\- Avoid easily discoverable security questions.

\- Use randomly generated password-reset tokens.

\- Make reset tokens single-use and short-lived.

\- Deliver recovery links through a verified recovery channel.

\- Consider MFA for account recovery.



\## Conclusion



The assessment demonstrated a weak password-recovery mechanism in an intentionally vulnerable training application. Testing was performed only within the authorized local lab environment.

