# Security Facts

## Security Boundaries
- **Main Threats:**
  - DDoS attacks (experienced previously)
  - General data intrusion
- **Mitigation:** Cloudflare for DDoS protection

## Password and Authentication
- **Password Requirements:**
  - Minimum length: 12 characters
  - No complex character requirements (no forced uppercase/lowercase/symbols)
  - Check against common passwords list
  - Encourage passphrases
  - Support password managers (allow very long passwords, special characters)
- **2FA:** Not implemented (low-risk data classification)
- **OAuth:** Implemented
- **API Keys:** Not planned currently

## Physical Security
- **Remote Work:** No specific requirements (team has no production access)
- **Public Places:** No restrictions on working from public places
- **Device Security:** No specific requirements for non-CEO devices

## Acceptable Use
- **Test Data:** No restrictions (not real data)
- **Production Data:** CEO access only, for debugging never testing

## Failed Login Handling
- Consider IP blocking for repeated failures
- No immediate alerting required

## Audit and Compliance
- **Audit Log Retention:** 1 year for administrative actions
- **Administrative Actions to Log:**
  - Changes to user permissions or roles
  - Creation/deletion of user accounts
  - Configuration changes to production systems
  - Access to sensitive data
  - Security policy modifications
  - Database schema changes
  - API key creation/revocation
- **Log Retention:**
  - Security logs: 1 year
  - Application logs: 90 days
- **Supplier Security:**
  - Annual review of supplier security certifications (CEO responsibility)
  - Document supplier ISO 27001 compliance status