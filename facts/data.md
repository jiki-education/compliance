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
- **Lawful Basis for Processing:** Contract (necessary to provide service)
- **Automated Decision-Making:** None currently (future: will add disclosures if implemented)
- **Profiling:** None currently (future: will add disclosures if implemented)

## Data Subject Rights
- **Access Requests:** Email to data@jiki.io
- **Deletion Requests:** Delete account button on website (TODO: implement)
- **Portability Requests:** Same mechanism as deletion
- **Response Time:** 30 days (GDPR compliant)

## Data Breach Response
- **Procedure:** CEO investigates, contains breach, documents incident
- **Internal Notification:** Whole team informed
- **External Notification:** Affected users + ICO (only if personal data stolen)
- **Timeline:** Within 72 hours to ICO, immediate to affected users
- **Documentation:** GitHub issue

## Age Restrictions
- **Minimum Age:** 13+ (stated in Terms & Conditions)
- **Verification:** No checkbox required
- **Under 13 Discovery:** Account deleted if user found to be under 13

## Marketing Communications
- **Current Status:** No marketing emails sent
- **Opt-in:** Checkbox at signup, account settings
- **Opt-out:** Unsubscribe link, account settings
- **Data Used:** None (no marketing activity)

## Data Access
- **Production Data Access:** CEO only
- **Access Controls:** MFA, IP restrictions
- **Purpose:** Debugging only, never for testing
- **Test Data:** No restrictions (not real data)

## Data Minimization
- **Decision Process:** CEO decides what data to collect based on feature requirements
- **Review Frequency:** When adding new features

## Third-Party Data Processing
- **Payment Processing:** Stripe (payment processor)
- **Storage:** AWS (data processor - Aurora database in eu-west-2)
- **Data Sharing:** No partnerships or data sharing agreements
- **Data Sales:** User data never sold or shared for marketing
- **International Transfers:** None to third parties (data only sent to users in their locations via normal website delivery)
- **No B2B DPA template currently**