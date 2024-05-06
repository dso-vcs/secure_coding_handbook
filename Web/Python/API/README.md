# Table of contents

<hr>

<details>
<summary>Authentication</summary>
<br>

**Login**
- [Improper Authentication](Vuln/improper_authentication.md)
- [Improper Restriction of Excessive Authentication Attempts](Vuln/improper_restriction_attempts.md)

**Change Password**
- [Unverified Password Change](Vuln/unverified_password_change.md)

**Forget Password**
- [Verify password credential recovery reveals the current password](Vuln/verify_password.md)

</details>

<br>

<details>
<summary>Session</summary>

- [Cleartext Transmission of Session Token](Vuln/cleartext_session_token.md)
- [Session Fixation](Vuln/session_fixation.md)
- [Insufficient Session Expiration](Vuln/insufficient_session_expiration.md)
- [Sensitive Cookie in HTTPS Session Without 'Secure' Attribute](Vuln/sensitive_cookie_without_secure_attribute.md)
- [Use of Hard-coded Password/Credentials](Vuln/use_of_hardcoded_password.md)

</details>

<br>

<details>
<summary>Access Control</summary>

- [IDOR](Vuln/idor.md)
- [Cross-Site Request Forgery (CSRF)](Vuln/csrf.md)
- [Missing Authorization](Vuln/missing_authorization.md)
- [Incorrect Authorization](Vuln/incorrect_authorization.md)

</details>

<br>

<details>
<summary>Validation, Sanitization and Encoding</summary>
<br>

**Input Validation**
- [Mass Assignment](Vuln/mass_assignment.md)
- [Open Redirect](Vuln/open_redirect.md)

**Sanitization and Sandboxing**
- [Improper Encoding or Escaping of Output](Vuln/improper_encoding_or_escaping.md)
- [Eval Injection](Vuln/eval_injection.md)
- [Code Injection](Vuln/code_injection.md)
- [SSRF](Vuln/ssrf.md)

**Output Encoding and Injection**
- [XSS](Vuln/XSS.md)
- [SQL Injection](Vuln/sql_injection.md)
- [OS Command Injection](Vuln/os_command_injection.md)
- [LFI](Vuln/lfi.md)
- [RFI](Vuln/rfi.md)
- [XPath Injection](Vuln/xpath_injection.md)

**Deserialization**
- [Deserialization of Untrusted Data](Vuln/deserialization_of_untrusted_data.md)
- [XXE](Vuln/xxe.md)
- [Eval Injection](Vuln/eval_injection.md)
</details>

<br>

<details>
<summary>Cryptography</summary>

- [Broken or Risky Crypto Algorithm](Vuln/broken_or_risky_crypto.md)
- [Use of Hard-coded Password/Credentials](Vuln/use_of_hardcoded_password.md)
</details>

<br>

<details>
<summary>Error Handling and Logging</summary>

- [Sensitive Information into Log File](Vuln/sensitivity_information_into_log_file.md)
- [Improper Output Neutralization for Logs](Vuln/improper_output_neutralization.md)
- [Insufficient Logging](Vuln/insufficient_logging.md)
- [Generation of Error Message Containing Sensitive Information](Vuln/generation_of_error_message_containing_sensitive_information.md)
- [Exposure of sensitive information](Vuln/exposure_of_sensitive_information.md)

</details>

<br>

<details>
<summary>Data Protection</summary>

- [Use of Web Browser Cache Containing Sensitive Information](Vuln/web_cache_containing_sensitive_information.md)
- [Insecure Storage of Sensitive Information](Vuln/insecure_storage_of_sensitive_information.md)
- [Cleartext Transmission of Sensitive Information](Vuln/cleartext_session_token.md)
</details>

<br>

<details>
<summary>Files Handling</summary>

- [Data Amplification](Vuln/data_amplification.md)
- [Unrestricted Upload of File with Dangerous Type](Vuln/unrestricted_file_upload)
- [Inclusion of Functionality from Untrusted Control Sphere](Vuln/inclusion_of_functionality_from_untrusted_control_sphere.md)
- [Path Traversal](Vuln/path_traversal.md)
- [External Control of File Name or Path](Vuln/external_control_of_file_name.md)
- [LFI](Vuln/lfi.md)
- [RFI](Vuln/rfi.md)
- [OS Command Injection](Vuln/os_command_injection.md)
- [SSRF](Vuln/ssrf.md)
</details>

<br>

<details>
<summary>API and Web Services</summary>

- [Improper Encoding or Escaping of Output](Vuln/improper_encoding_or_escaping.md)
- [Use of GET Request Method With Sensitive Query Strings](Vuln/get_request_with_sensitive_query_string.md)
- [Trusting HTTP Permission Methods on the Server Side](Vuln/trusting_http_permission.md)
- [CSRF](Vuln/csrf.md)
</details>
