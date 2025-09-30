# Data Protection Policy

**Last Modified:** September 2025
**Document Owner:** Jeremy Walker, Chief Executive Officer
**Version:** 1.0
**Classification:** Internal

## Purpose

This Data Protection Policy establishes Jiki's commitment to protecting personal data and outlines our approach to data protection in accordance with GDPR principles. This policy ensures that personal data is collected, processed, stored, and deleted in a lawful, fair, and transparent manner.

## Scope

This policy applies to all personal data processed by Jiki, including:
- User personal data (email, name)
- Learning progress data
- User code submissions
- Any other data that identifies or could identify an individual

This policy applies to all employees, contractors, and third parties who process personal data on behalf of Jiki.

## Principle

Personal data shall be processed lawfully, fairly, and transparently, with appropriate security measures to protect the rights and freedoms of individuals.

## Chief Executive Statement of Commitment

I am committed to protecting the personal data entrusted to Jiki by our users. This Data Protection Policy demonstrates our commitment to data protection principles and GDPR compliance, ensuring that personal data is handled with the highest standards of care and security.

**Jeremy Walker**
Chief Executive Officer
Date:

## Introduction

Data protection is fundamental to maintaining user trust and meeting our legal obligations. Jiki voluntarily adheres to GDPR principles to ensure that personal data is protected throughout its lifecycle. This policy provides a framework for:

- Lawful and transparent data processing
- Protecting individual rights
- Ensuring data security
- Managing data breaches
- Demonstrating accountability

## Roles and Responsibilities

### Data Protection Officer (DPO)
**Role holder:** Jeremy Walker, Chief Executive Officer

Responsibilities:
- Oversee data protection strategy and implementation
- Monitor compliance with GDPR principles and this policy
- Serve as primary contact for data protection matters
- Handle data subject requests
- Manage data breach response
- Maintain data protection documentation

### All Employees
Responsibilities:
- Process personal data only as authorized
- Report suspected data breaches immediately to the DPO
- Complete data protection training
- Follow data handling procedures

## Data Protection Principles

Jiki adheres to the following GDPR data protection principles:

### 1. Lawfulness, Fairness, and Transparency
- Personal data is processed lawfully under the basis of **contract** (processing is necessary to provide the service)
- Users are informed about how their data is used through our Privacy Policy
- Data processing is transparent and clearly communicated

### 2. Purpose Limitation
- Personal data is collected for specific, explicit, and legitimate purposes
- Data is not processed in a manner incompatible with those purposes
- Users are informed of the purpose at the point of collection

### 3. Data Minimization
- Only personal data that is necessary for the specified purpose is collected
- The CEO reviews data necessity when adding new features
- Unnecessary data collection is avoided

### 4. Accuracy
- Reasonable steps are taken to ensure personal data is accurate
- Inaccurate data is corrected or deleted without delay
- Users can update their personal information through their account settings

### 5. Storage Limitation
- Personal data is retained only as long as necessary for the specified purpose
- Retention periods are defined in the Data Retention Policy
- Data is securely deleted when no longer needed

### 6. Integrity and Confidentiality (Security)
- Appropriate technical and organizational measures protect personal data
- Data is protected against unauthorized or unlawful processing, accidental loss, destruction, or damage
- Security measures are regularly reviewed and updated

### 7. Accountability
- Jiki is responsible for and can demonstrate compliance with data protection principles
- Records of processing activities are maintained
- Data protection impact assessments are conducted when required

## Lawful Basis for Processing

Jiki processes personal data under the following lawful basis:

**Contract:** Processing is necessary to provide the learning platform service to users. This includes:
- Creating and managing user accounts
- Delivering learning content
- Tracking learning progress
- Communicating service-related information
- Processing payments (via Stripe)

## Data Subject Rights

Jiki respects and facilitates the following data subject rights:

### Right of Access
Users have the right to obtain confirmation that their personal data is being processed and access to that data.

**How to exercise:** Email data@jiki.io
**Response time:** Within 30 days

### Right to Rectification
Users have the right to have inaccurate personal data corrected.

**How to exercise:** Update information in account settings or email data@jiki.io
**Response time:** Without undue delay

### Right to Erasure ("Right to be Forgotten")
Users have the right to have their personal data deleted in certain circumstances.

**How to exercise:** Use the "Delete Account" button on the website
**Response time:** Immediate deletion from production; retained in backups for 30 days
**Note:** Account deletion button to be implemented (documented in technical TODOs)

### Right to Data Portability
Users have the right to receive their personal data in a structured, commonly used, machine-readable format.

**How to exercise:** Use the data export function on the website or email data@jiki.io
**Response time:** Within 30 days
**Format:** JSON or CSV

### Right to Object
Users have the right to object to processing of their personal data in certain circumstances.

**How to exercise:** Email data@jiki.io
**Response time:** Within 30 days
**Note:** As processing is based on contract, objection may result in inability to provide service

### Right to Restrict Processing
Users have the right to restrict processing of their personal data in certain circumstances.

**How to exercise:** Email data@jiki.io
**Response time:** Within 30 days

### Rights Related to Automated Decision-Making and Profiling
**Current status:** Jiki does not currently engage in automated decision-making or profiling.
**Future implementation:** If automated decision-making or profiling is implemented, users will be informed and appropriate rights will be documented and implemented.

## Data Security Measures

Jiki implements the following technical and organizational measures to protect personal data:

### Technical Measures
- **Encryption at rest:** All data stored in Aurora database is encrypted
- **Encryption in transit:** All data transmitted is encrypted using HTTPS/TLS
- **Access controls:**
  - Production data access restricted to CEO only
  - Multi-factor authentication (MFA) required
  - IP restrictions on database access
- **Secure authentication:** Password requirements per Password and Authentication Policy
- **Audit logging:** Administrative actions logged and retained for 1 year

### Organizational Measures
- **Access limitation:** Only CEO has production data access, for debugging purposes only
- **Data minimization:** Only necessary data is collected
- **Regular reviews:** Security measures reviewed annually
- **Incident response:** Documented procedures for data breach response
- **Training:** All employees receive data protection training

## Data Breach Management

A personal data breach is a breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorized disclosure of, or access to personal data.

### Detection and Reporting
- All employees must report suspected data breaches immediately to the DPO (CEO)
- Reports can be made via email or direct communication
- All suspected breaches are logged in GitHub issues for investigation

### Assessment
The DPO will assess the breach to determine:
- Nature and scope of the breach
- Data affected
- Number of individuals affected
- Potential consequences
- Whether notification is required

### Notification Requirements

**To Supervisory Authority (ICO):**
- Required if personal data has been stolen or there is a risk to individuals' rights and freedoms
- Notification within 72 hours of becoming aware of the breach
- Method: ICO online reporting tool

**To Affected Individuals:**
- Required if breach is likely to result in high risk to individuals' rights and freedoms
- Notification without undue delay
- Method: Email to affected users

**Internal Notification:**
- Whole team informed of breach and response actions

### Containment and Recovery
1. CEO investigates and contains the breach
2. Affected systems isolated if necessary
3. Vulnerabilities identified and remediated
4. Recovery actions implemented
5. Post-incident review conducted

### Documentation
All data breaches are documented in GitHub issues, including:
- Nature of the breach
- Data affected
- Individuals affected
- Actions taken
- Notifications made
- Lessons learned

## Data Transfers

### International Transfers
Jiki does not transfer personal data to third parties outside the UK/EU.

Personal data is transmitted to users in their countries through normal website delivery (HTTPS), which is not considered an international transfer under GDPR.

### Third-Party Data Processors
Jiki uses the following third-party data processors:
- **AWS:** Data storage (Aurora database in London region, eu-west-2)
- **Stripe:** Payment processing

All data processors are required to implement appropriate technical and organizational measures to protect personal data.

## Data Sharing

- Jiki does not sell or share personal data for marketing purposes
- Jiki does not have data sharing partnerships or agreements
- Personal data is only shared with data processors necessary to provide the service
- Users are informed of third-party processors in the Privacy Policy

## Children's Data

### Age Restrictions
- Jiki's services are intended for users aged 13 and over
- This age restriction is stated in the Terms & Conditions
- No age verification checkbox is required at signup

### Discovery of Under-Age Users
If Jiki becomes aware that a user is under 13 years old:
1. The user's account will be deleted immediately
2. All associated personal data will be deleted from production
3. Data will remain in backups for the standard retention period (30 days)

## Marketing Communications

### Current Status
Jiki does not currently send marketing emails.

### Future Marketing (if implemented)
If marketing communications are implemented:

**Opt-in:**
- Checkbox at signup (unchecked by default)
- Option in account settings

**Opt-out:**
- Unsubscribe link in all marketing emails
- Option in account settings

**Data used:**
- Email address only
- No profiling or behavioral targeting

## Data Protection Impact Assessments (DPIA)

A DPIA is required when:
- Implementing new data processing activities that are likely to result in high risk to individuals
- Significant changes to existing processing activities
- Implementing automated decision-making or profiling
- Processing special category data at scale

DPIAs are conducted by the DPO (CEO) and documented before processing begins.

## Records of Processing Activities

Jiki maintains records of processing activities including:
- Purposes of processing
- Categories of data subjects
- Categories of personal data
- Categories of recipients
- Data retention periods
- Security measures

Records are maintained by the DPO and reviewed annually.

## Training and Awareness

All employees receive:
- Initial data protection training during onboarding
- Mandatory review of this policy
- Annual data protection discussion with CEO
- Updates when data protection practices change

## Policy Review

This policy is reviewed annually by the CEO and updated as necessary to reflect:
- Changes in data processing activities
- Changes in legal requirements
- Lessons learned from incidents
- Best practice developments

## Related Policies

- Information Security Policy
- Data Retention Policy
- Access Control Policy
- Password and Authentication Policy
- Acceptable Use Policy
- Incident Response Policy

## Contact

For questions about this policy or data protection matters:

**Data Protection Officer:** Jeremy Walker
**Email:** data@jiki.io

## Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | September 2025 | Jeremy Walker | Initial policy creation |