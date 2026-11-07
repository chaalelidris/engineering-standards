# Engineering Standards

A practical, stack-agnostic collection of checklists and templates for designing, building, reviewing, and operating reliable software.

These standards are intended to be tailored to the risk, scale, and context of each project. They are decision aids—not a substitute for engineering judgment.

## Contents

### Engineering standards
- [System Design Review](.github/standards/system-design.md)
- [Security Review Checklist](.github/standards/security-checklist.md)
- [Production Readiness Review](.github/standards/production-readiness.md)

### GitHub templates
- [Feature request](.github/ISSUE_TEMPLATE/feature.md)
- [Bug report](.github/ISSUE_TEMPLATE/bug_report.md)
- [Security review](.github/ISSUE_TEMPLATE/security_review.md)
- [Pull request template](.github/pull_request_template.md)

## Recommended workflow

1. **Define the change.** Create an issue for meaningful features, defects, and operational work.
2. **Design proportionately.** Use the system design checklist when a change affects architecture, data, integrations, availability, or scale.
3. **Review security early.** Apply the security checklist whenever a change touches identity, authorization, sensitive data, external input, infrastructure, or dependencies.
4. **Prepare to operate it.** Use the production-readiness checklist before a new service or material production change is released.
5. **Record evidence.** Link decisions, tests, dashboards, threat models, runbooks, and deployment plans rather than checking boxes without proof.
6. **Revisit after release.** Capture incidents and operational lessons in follow-up issues or architecture decision records.

## How to use the checklists

- Mark an item complete only when there is evidence.
- Mark an item not applicable when it genuinely does not apply; add a short reason for material exclusions.
- Assign an owner to unresolved high-risk items.
- Do not treat a checklist score as an automatic approval.
- Scale the depth of review to the impact and risk of the change.

## Review cadence

Review these standards periodically and after significant incidents, security findings, platform changes, or recurring delivery problems. Adapt them to the organization's regulatory, contractual, and operational obligations.

## Security reporting

Do not publish credentials, personal data, exploit details, or unpatched vulnerability information in public issues. Use the repository owner's private security reporting process where available.

## License

No license is granted by this repository unless a license file is added. Add an explicit open-source license before permitting reuse, modification, or redistribution.
