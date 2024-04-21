# Table of contents

<hr>

<details>
<summary>Authentication</summary>

**Login**
- [Improper Authentication](vuln/improper_authentication.md)
- Improper Restriction of Excessive Authentication Attempts

**Change Password**
- [Unverified Password Change](vuln/unverified_password_change.md)

**Forget Password**
- Verify password credential recovery does not reveal the current 
password in any way.

</details>

<br>

<details>
<summary>Session</summary>

- Cleartext Transmission of Session Token
- [Session Fixation](vuln/session_fixation.md)
- Insufficient Session Expiration
- [Sensitive Cookie in HTTPS Session Without 'Secure' Attribute](vuln/sensitive_cookie_without_secure_attribute.md)
- [Use of Hard-coded Password/Credentials](vuln/Use_of_Hardcoded_Password.md)

</details>

<br>

<details>
<summary>Access Control</summary>

- [IDOR](vuln/idor.md)
- [Cross-Site Request Forgery (CSRF)](vuln/CSRF.md)
- [Missing Authorization](vuln/Missing_authorization.md)
- [Incorrect Authorization](vuln/Incorrect_authorization.md)

</details>

<br>

<details>
<summary>Validation, Sanitization and Encoding</summary>

**Input Validation**
- Mass Assignment
- Open Redirect

**Sanitization and Sandboxing**
- Improper Encoding or Escaping of Output
- Eval Injection
- Code Injection
- [SSRF](vuln/ssrf.md)

**Output Encoding and Injection**
- [XSS](vuln/XSS.md)
- [SQL Injection](vuln/SQL_Injection.md)
- OS Command Injection
- LFI - RFI
- XPath Injection

**Deserialization**
- [Deserialization of Untrusted Data](vuln/deserialization_of_untrusted_data.md)
- XXE
- Eval Injection
</details>

<br>

<details>
<summary>Cryptography</summary>

- [Broken or Risky Crypto Algorithm](vuln/Broken_or_risky_crypto.md)
- [Use of Hard-coded Password/Credentials](vuln/Use_of_Hardcoded_Password.md)
</details>

<br>

<details>
<summary>Error Handling and Logging</summary>

- [Sensitive Information into Log File](vuln/sensitivity_information_into_log_file.md)
- [Improper Output Neutralization for Logs](vuln/improper_output_neutralization.md)
- [Insufficient Logging](vuln/insufficient_logging.md)
- [Generation of Error Message Containing Sensitive Information](vuln/generation_of_error_message_containing_sensitive_information.md)
- [Exposure of sensitive information](vuln/Exposure_Of_Sensitive_Information.md)

</details>

<br>

<details>
<summary>Data Protection</summary>

- Use of Web Browser Cache Containing Sensitive Information
- Insecure Storage of Sensitive Information
- Cleartext Transmission of Sensitive Information
</details>

<br>

<details>
<summary>Files Handling</summary>

- Data Amplification
- Unrestricted Upload of File with Dangerous Type
- [Inclusion of Functionality from Untrusted Control Sphere](vuln/inclusion_of_functionality_from_untrusted_control_sphere.md)
- [Path Traversal](vuln/Path_Traversal.md)
- [External Control of File Name or Path](vuln/external_control_of_file_name.md)
- LFI
- RFI
- OS Command Injection
- SSRF
</details>

<br>

<details>
<summary>API and Web Services</summary>

- Improper Encoding or Escaping of Output
- Use of GET Request Method With Sensitive Query Strings
- Trusting HTTP Permission Methods on the Server Side
- CSRF
</details>
