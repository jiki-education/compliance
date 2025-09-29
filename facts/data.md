# Data Facts

## Data Types Handled
- User personal data (email and name only)
- No GDPR-protected special category data
- Learning progress data
- User code submissions
- Payment information (handled by Stripe)

## Data Retention
- **User Account Deletion:** Immediate deletion from production
- **Backup Retention:** Data retained in backups for 30 days
- **User Code:** Deleted (if personal) or anonymized (if non-personal) on account deletion
- **Audit Logs:** 1 year retention (administrative actions)

## Data Classification Scheme
1. **Public:** Marketing content, public documentation
2. **Internal:** Team docs, meeting notes
3. **Confidential:** User data, source code
4. **Restricted:** Passwords, API keys

## Data Residency
- **Storage Location:** London region (eu-west-2)
- **Geographic Scope:** Worldwide operation
- **Data Residency Requirements:** None beyond storing in London

## Data Protection
- **GDPR Compliance:** Voluntary adherence
- **Special Category Data:** None collected
- **Analytics:** Currently none (future implementation planned)

## Data Access
- **Production Data Access:** CEO only
- **Purpose:** Debugging only, never for testing
- **Test Data:** No restrictions (not real data)

## Third-Party Data Processing
- **Payment Processing:** Stripe
- **No B2B DPA template currently**