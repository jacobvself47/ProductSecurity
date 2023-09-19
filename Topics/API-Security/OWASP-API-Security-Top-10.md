# OWASP API Security Top 10

[Link to 2023 Documentation](https://owasp.org/API-Security/editions/2023/en/0x00-header/)

## 1 - Broken Object Level Authorization
### Risk Information
- Easily Exploitable
- Widespread Prevelance
- Impacts information disclosure, modification, or destruction of all data
### Details
- Object level authorization: code-level access control to validate permissions
- All API endpoints should implement object-level authorization checks
- Validate logged-in user has permissions to perform the requested action on the requested object
### How to Prevent
- Implement and enforce the use of an authorization mechanism for every function that uses an input from the client
- Use GUIDs to make object values unpredictable
### Simple Summary
Broken Object Level Authorization (BOLA) is easily exploitable and highly prevelant.  The vulnerability occurs when an object does not check the logged-in user's authorization before granting access.  An attacker can exploit a vulnerable endpoint by manipulating the object ID sent within the request.  This vulnerability can lead to unauthorized access to information.  It can be prevented by enforcing authorization checks for all objects.

## 2 - Broken Authentication
### Risk Information
- Easily Exploitable
- Common Prevelance
- Severe impact - complete control of other users' accounts
### Details
- Authentication endpoints are assets that need to be protected
- The API is vulnerable if authentication controls are poor.
- Below are examples of poor authentication controls
  - Brute force attacks on the authentication endpoint
    - Credential stuffing - brute force with a list of valid usernames and passwords
    - Brute force attacks on the same user account
  - Weak passwords
  - Sensitive authentication details in th URL - auth tokens and passwords in plain text
  - Not requiring password confirmation for changes to email addressess or passwords
  - Lack of validation against the authenticity of tokens
  - Poor JWT token controls
    - accepts weakly signed JWT tokens
    - Lack of JWT expiration dat validation
### How to Prevent
- Review all flows to authenticate to the AI
- Use industry standards for authentication, token generation, or password storage
- Require re-authentication for sensitive operations
- Implement MFA
- Implement anit-burte force mechanisms to mitigate credential stuffing, dictionary attaks, and brute force attacts.
- Authentication flows should have more strict rate limiting that other APIs
### Simple Summary
Broken Authentication is a high risk vulnerability that would allow an attacker to gain unauthorized access to user accounts.  The way to mitigate this risk is to implement industry-standard controls for protecting authorization flows.  These include: MFA, strict rate limiting for auth flow, protection and validation of JWT tokens, and preventing easily identifiable authentication details.

## 3 - Broken Object Property Level Authorization
### Risk Information
### Details
### How to Prevent
### Simple Summary

## 4 - Unrestricted Resource Consumption
### Risk Information
### Details
### How to Prevent
### Simple Summary

## 5 - Broken Function Level Authorization
### Risk Information
### Details
### How to Prevent
### Simple Summary

## 6 - Unrestricted Access to Sensitive Business Flows
### Risk Information
### Details
### How to Prevent
### Simple Summary

## 7 - Server Side Request Forgery
### Risk Information
### Details
### How to Prevent
### Simple Summary

## 8 - Security Misconfiguration
### Risk Information
### Details
### How to Prevent
### Simple Summary

## 9 - Improper Inventory Management
### Risk Information
### Details
### How to Prevent
### Simple Summary

## 10 - Unsafe Consumption of APIs
### Risk Information
### Details
### How to Prevent
### Simple Summary
