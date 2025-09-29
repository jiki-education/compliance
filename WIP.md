# Information Security Policy - Information Gathering (WIP)

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

## COMPLETED CLARIFICATIONS

All questions have been answered. Ready to proceed with policy creation.

## NEXT STEPS

1. Create facts folder with source of truth documentation
2. Update AGENTS.md with facts folder instructions
3. Draft Information Security Policy
4. Update control A.5.1 in organizational-controls.md
5. Create incident response procedures document
6. Create business continuity plan document