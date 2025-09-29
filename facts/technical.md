# Technical Facts

## Infrastructure

### AWS Infrastructure
- **Primary Region:** London (eu-west-2)
- **Database:** Aurora Serverless v2
- **API Hosting:** AWS Fargate
- **Email Service:** AWS SES

### Other Infrastructure
- **Frontend Hosting:** Cloudflare Workers for Next.js
- **CDN:** Cloudflare
- **DDoS Protection:** Cloudflare
- **Code Repository:** GitHub
- **CI/CD:** GitHub Actions (GHA)
- **Error Tracking:** Bugsnag (may change)

### Services Not Used
- Customer support platforms
- Analytics (future implementation planned)
- Staging environment

## Access Control

### Production Access
- **Who:** CEO only
- **How:** VPN with dedicated IP (accessible only from CEO's laptop)
- **Bastion:** IP-restricted bastion host
- **AWS Console:** CEO only
- **Credentials:** Not shared with team

### Development Access
- Developers use local machines
- Local test environments
- CI testing via GitHub Actions

## Authentication
- Password-based authentication
- OAuth integration
- No 2FA (low-risk data classification decision)
- No API keys for programmatic access currently

## Deployment Process
- GitHub PRs with review required
- CEO approves production deployments
- On-demand deployments
- Multiple deployments on work days typical

## Data Storage
- Aurora Serverless v2 in London region
- Encryption at rest (to be verified and configured)

## Backup Configuration
- **Retention Period:** 30 days
- **Point-in-Time Recovery:** Last 7 days
- **Testing Frequency:** Quarterly
- **Recovery Time Objective (RTO):** 4 hours
- **Recovery Point Objective (RPO):** 1 hour

## Security Monitoring
- **Current State:** No monitoring implemented
- **Future:** AWS-specific monitoring to be implemented

## Incident Response Times
- **Critical** (data breach, platform down): 1 hour response
- **High** (security vulnerability, partial outage): 4 hours response
- **Medium** (suspicious activity, performance issues): 24 hours response
- **Low** (minor bugs, documentation): 1 week response
- Note: Response = acknowledgment, not resolution

## Historical Context
- Previous DDoS attacks experienced
- Mitigation now via Cloudflare