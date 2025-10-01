# Jiki Compliance Repository

## Purpose

This repository serves as the central hub for all compliance-related documentation and data collection for Jiki, with a primary focus on achieving ISO 27001 certification. It maintains a comprehensive record of security-related facts, policies, procedures, and evidence needed for information security management.

## Repository Structure

```
compliance/
├── README.md                 # This file
├── AGENTS.md                 # Instructions for AI agents working in this repo
├── CLAUDE.md                 # Symlink to AGENTS.md
├── ISO27001-summary.md       # Human-readable overview of ISO 27001 requirements
├── facts/                    # Authoritative data collected from other repos
│   ├── technical/           # Technical architecture and security controls
│   ├── organizational/      # Organizational structure and policies
│   ├── operational/         # Operational procedures and evidence
│   └── third-party/         # Third-party services and assessments
├── policies/                 # Security policies and procedures
├── risk-assessment/          # Risk registers and treatment plans
├── controls/                 # Implementation status of Annex A controls
├── evidence/                 # Audit evidence and compliance artifacts
└── reports/                  # Audit reports and management reviews
```

## Key Objectives

1. **Compliance Tracking**: Maintain comprehensive documentation for ISO 27001 certification
2. **Fact Collection**: Gather authoritative data from parallel Jiki repositories
3. **Risk Management**: Document and track information security risks
4. **Control Implementation**: Track the implementation of security controls
5. **Audit Preparation**: Organize evidence for certification audits
6. **Continuous Improvement**: Document lessons learned and improvement actions

## How This Repository Works

### Data Collection

This repository collects facts from multiple sources:
- **Technical Repository**: Architecture decisions, security implementations, technical controls
- **Overview Repository**: Business strategy, organizational structure, product vision
- **Operational Data**: Live system metrics, incident reports, performance data
- **Human Input**: Policy decisions, risk assessments, management reviews

### Documentation Standards

All documentation in this repository follows these principles:
- **Authoritative**: Only verified, accurate information
- **Traceable**: Clear references to sources and evidence
- **ISO 27001 Aligned**: Structured to support certification requirements
- **Version Controlled**: All changes tracked through git
- **Clear and Concise**: Written for both technical and non-technical audiences

### Working with AI Agents

AI agents working in this repository should:
1. Collect data from other Jiki repositories
2. Document facts in a structured, ISO 27001-compatible format
3. Maintain traceability to source information
4. Flag any compliance gaps or risks identified
5. Generate reports and summaries as needed

See [AGENTS.md](./AGENTS.md) for detailed instructions.

## Integration with Jiki Ecosystem

This compliance repository interfaces with:

- **jiki/overview**: Strategic direction and business context
- **jiki/tech**: Technical implementation details
- **jiki/platform**: Production system information
- **jiki/operations**: Operational procedures and metrics

## Compliance Scope

The ISO 27001 ISMS scope for Jiki includes:

- The Jiki learning platform and all its components
- User data (personal information, learning progress, payments)
- Content management and delivery systems
- Integration with Exercism
- Supporting infrastructure and services

## Key Stakeholders

- **Chief Information Security Officer (CISO)**: Overall ISMS responsibility
- **Development Team**: Technical control implementation
- **Operations Team**: Operational security and monitoring
- **Management Team**: Strategic direction and resource allocation
- **External Auditors**: Certification assessment

## Important Dates and Milestones

- **Q4 2024**: Initial compliance assessment and gap analysis
- **Q1 2025**: Platform launch with core security controls
- **Q2 2025**: First internal ISMS audit
- **Q3 2025**: Pre-certification assessment
- **Q4 2025**: ISO 27001 certification audit

## Getting Started

1. Review [ISO27001-summary.md](./ISO27001-summary.md) for an overview of requirements
2. Check the `facts/` directory for current documented information
3. See [AGENTS.md](./AGENTS.md) for instructions on data collection
4. Review existing policies in the `policies/` directory
5. Check `risk-assessment/` for current risk status

## Contributing

When adding information to this repository:

1. Ensure all facts are verified and sourced
2. Follow the existing directory structure
3. Update relevant indexes and cross-references
4. Include evidence where applicable
5. Flag any identified compliance gaps

## Compliance Status

Current ISO 27001 readiness: **Planning Phase**

Key areas of focus:
- [ ] ISMS scope definition
- [ ] Risk assessment methodology
- [ ] Security policy development
- [ ] Control selection and implementation
- [ ] Documentation framework
- [ ] Audit preparation

## Contact

For questions about compliance or this repository, contact the Jiki security team.

## Related Documentation

- [Jiki Overview Repository](../overview/README.md)
- [ISO 27001 Standard](https://www.iso.org/standard/82875.html)
- [ISO 27001 Summary](./ISO27001-summary.md)
- [Agent Instructions](./AGENTS.md)

---

Copyright (c) 2025 Jiki Ltd. All rights reserved.