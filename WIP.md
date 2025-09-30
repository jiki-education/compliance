# Data Protection Policy - Information Gathering (WIP)

## 1. Organizational Context

**Team Structure:**
- Jeremy Walker - CEO (also serves as Information Security Officer and Data Protection Officer)
- Aron Dementer - Front end developer
- Nicole Chalmers - Head of Product

**External Access:**
- No external contractors or third parties have system access

## 2. Scope of Information Security

**Data Types Handled:**
- User personal data (email and name only)
- No GDPR-protected special category data
- Learning progress data
- User code submissions
- Payment information (via Stripe)

**Systems in Scope:**
- Production platform (Cloudflare Workers, Fargate, Aurora)
- Email systems (AWS SES)
- Development environments (local machines)
- CI/CD pipeline (GitHub Actions)

**Exclusions:**
- None

## 3. Current Security Practices

**Authentication:**
- Password-based authentication
- OAuth integration
- No 2FA (decision based on low-risk data classification)

**Data Storage:**
- Amazon Aurora Serverless v2 database in London region (eu-west-2)
- Encryption at rest: TBD (add to TECH_TODO.md)

**Backups:**
- Aurora Serverless v2 automated backups
- Retention: 30 days
- Point-in-time recovery: Last 7 days
- Backup testing: Quarterly
- RTO: 4 hours
- RPO: 1 hour

**Security Monitoring:**
- Currently: None
- TO IMPLEMENT: AWS-specific monitoring solutions (in TECH_TODO.md)

**Production Access Management:**
- Only CEO has access via:
  - VPN with dedicated IP (accessible only from CEO's laptop)
  - IP-restricted bastion host
  - AWS console access
- Developers have access to development environments only
- Credentials not shared with team

**Incident Response:**
- Response = acknowledgment, not resolution
- Incident severity levels:
  - Critical (data breach, platform down): Response within 1 hour
  - High (security vulnerability, partial outage): Response within 4 hours
  - Medium (suspicious activity, performance issues): Response within 24 hours
  - Low (minor bugs, documentation): Response within 1 week

## 4. Risk Management Approach

**Review Frequency:** Annual

**Risk Assessment Team:** CEO

**Risk Appetite:** Cautious

## 5. Compliance and Legal

**Compliance Requirements:**
- ISO 27001 (target certification)
- GDPR adherence (voluntary compliance)
- No PCI-DSS (Stripe handles payment card data)

**Geographic Scope:** Worldwide operation

**Data Residency:** London region (eu-west-2)

**Partner Requirements:** None currently

**DPA:** No B2B DPA template currently

## 6. Security Objectives

**Top Priorities:**
1. Protecting all user data from unauthorized access/intrusion
2. Ensuring platform availability and resilience against DDoS attacks
3. Protecting payment information (delegated to Stripe)

**Historical Context:**
- Previous DDoS attacks experienced (mitigation via Cloudflare)

## 7. Policy Management

**Review Cycle:** Annual

**Approval Authority:** CEO

**Communication Method:** Documentation system (internal docs)

## 8. Incident Response

**Incident Handler:** CEO

**Response Times:** See incident severity levels above

**Notifications:** Internal team only

**External Communications:**
- Status page for users (TO IMPLEMENT - in TECH_TODO.md)
- Security email: security@jiki.io (TO IMPLEMENT - in TECH_TODO.md)

**External Support:** No existing security vendor relationships

## 9. Business Continuity

**Acceptable Downtime:**
- Ideal: Zero downtime
- Tolerable: Few hours for critical issues

**Critical Functions:**
- Platform availability (not mission-critical but important)

**Disaster Recovery:**
- RTO: 4 hours
- RPO: 1 hour
- Testing frequency: Quarterly

## 10. Training and Awareness

**Team Communication:**
- Ad-hoc meetings when security changes occur

**Training Program:**
- Initial meeting for security overview
- Mandatory documentation review for new employees
- Updates communicated via meetings as needed

**Awareness Tracking:**
- Annual security discussion with CEO

## 11. Development and Deployment

**Development Environment:**
- Developers work on local machines
- Local test environments
- CI testing (no staging environment)

**Deployment Process:**
- GitHub Actions (GHA) for CI/CD
- GitHub PRs with review required
- CEO approves production deployments
- On-demand deployments (multiple times on work days)

**Infrastructure:**
- Cloudflare Workers for Next.js frontend
- AWS Fargate for API
- Aurora Serverless v2 for database
- Primary region: London (eu-west-2)

## 12. Data Handling

**Data Retention:**
- User account deletion: Immediate deletion from production
- Backup retention: Data retained in backups for backup duration (30 days)
- User code: Deleted (personal) or anonymized (non-personal) on account deletion

**Analytics:**
- Currently: None
- Future: TBD (added to TECH_TODO.md)

## 13. Third-Party Services

**Current Services:**
- GitHub (code repository and CI/CD)
- Cloudflare (CDN and DDoS protection)
- Stripe (payment processing)
- AWS SES (email service)
- Bugsnag (error tracking - may change, see TECH_TODO.md)

**Planned Services:**
- Analytics: TBD (added to TECH_TODO.md)

**Not Using:**
- Customer support platforms

## 14. Security Boundaries

**Specific Threats:**
- DDoS attacks (experienced previously)
- General data intrusion concerns
- No specific additional threats identified

## 15. Acceptable Use

**Test Data:**
- No restrictions on test data usage (not real data)

**Production Data:**
- Only CEO has access to production data
- Used for debugging only, never for testing

## 16. Cryptography

**Password Requirements:**
- TO BE DEFINED: Reasonable complexity without excessive restrictions
- No API keys for programmatic access planned currently

## 17. Audit and Logging

**Audit Log Retention:**
- Administrative actions: 1 year (standard)

**Failed Login Handling:**
- Consider IP blocking for repeated failures
- No immediate alerting required

## 18. Supplier Security

**Security Review:**
- Review supplier security certifications
- Document supplier ISO 27001 compliance status

## 19. Physical Security

**Remote Work Security:**
- No specific requirements for home offices (no production data access)
- No restrictions on working from public places (no production data access)

## 20. Information Classification

**Data Categories:**
- Public (marketing content, public docs)
- Internal (team docs, meeting notes)
- Confidential (user data, source code)
- Restricted (passwords, API keys)

## QUESTIONS FOR DATA PROTECTION POLICY

### Data Subject Rights (GDPR-aligned)
1. How do users request access to their data?
2. How do users request deletion of their data?
3. How do users request data portability (export)?
4. What is the response time target for these requests?

### Data Breach Handling
1. What is the procedure when a data breach is detected?
2. Who needs to be notified (internally and externally)?
3. What is the timeline for breach notification?
4. Where are breach incidents documented?

### Data Processing
1. What is the lawful basis for processing user data (consent, contract, legitimate interest)?
2. Are there any automated decision-making processes?
3. Is there any profiling of users?

### Data Transfers
1. Are there any international data transfers outside UK/EU?
2. If yes, what mechanisms are used (SCCs, adequacy decisions, etc.)?

### Third-Party Data Sharing
1. Beyond Stripe, are there any other third parties that receive user data?
2. Are there any data sharing agreements with partners?
3. Is user data ever sold or shared for marketing?

### Data Minimization
1. What is the process for determining what data to collect?
2. How often is data necessity reviewed?

### Data Security Measures (specific to data protection)
1. Is data encrypted at rest?
2. Is data encrypted in transit?
3. What access controls are in place for data?
4. Are there any data anonymization processes?

### Children's Data
1. Does Jiki have any age restrictions?
2. Is there a process to verify users are not children?

### Marketing and Communications
1. How do users opt-in/opt-out of marketing communications?
2. What data is used for marketing purposes?

## COMPLETION SUMMARY

✅ **Data Protection Policy Created**
- Document location: `/Users/iHiD/Code/jiki/compliance/policies/data-protection-policy.md`
- Version: 1.0
- Status: Complete

✅ **Facts Files Updated**
- `facts/data.md` - Added data subject rights, breach response, age restrictions, marketing, data minimization, encryption
- `facts/security.md` - Added encryption details

✅ **Technical TODOs Added**
- Implement "Delete Account" button on website
- Implement data export/portability function

✅ **Progress Tracker Updated**
- `todo.md` - Marked Data Protection Policy as complete
- Progress: 2/14 policies completed

## ANSWERS GATHERED

### Data Subject Rights
- **Access requests:** Email to data@jiki.io, 30-day response time
- **Deletion:** Delete account button on website (TODO: implement in TECH_TODO)
- **Portability:** Same mechanism as deletion
- **Response time:** 30 days (GDPR compliant)

### Data Breach Handling
- **Procedure:** CEO investigates, contains breach, documents incident
- **Notifications:** Affected users + ICO (only if personal data stolen)
- **Timeline:** Within 72 hours to ICO, immediate to affected users
- **Documentation:** GitHub issue

### Data Processing
- **Lawful basis:** Contract (processing necessary to provide service)
- **Automated decision-making:** None currently (future: TBD, will add disclosures if implemented)
- **Profiling:** None currently (future: TBD, will add disclosures if implemented)

### Data Transfers
- **International transfers:** None to third parties
- **User access:** Data sent to users in their countries (normal website delivery)

### Third-Party Data Sharing
- **Data processors:** AWS (storage), Stripe (payments)
- **Partnerships:** None
- **Marketing/Sales:** No data sold or shared for marketing

### Data Minimization
- **Decision process:** CEO decides based on feature requirements
- **Review frequency:** When adding new features

### Data Security
- **Encryption at rest:** Yes (Aurora)
- **Encryption in transit:** Yes (HTTPS/TLS)
- **Access controls:** CEO only, MFA, IP restrictions
- **Anonymization:** None implemented

### Children's Data
- **Age restriction:** 13+ in Terms & Conditions
- **Verification:** No checkbox required
- **Under 13 discovery:** Delete account if discovered

### Marketing Communications
- **Opt-in mechanisms:** Checkbox at signup, account settings
- **Opt-out mechanisms:** Unsubscribe link, account settings
- **Current status:** No marketing emails currently sent
- **Data used:** None (no marketing activity)