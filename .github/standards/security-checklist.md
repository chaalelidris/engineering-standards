# Security Review Checklist

Use this checklist when introducing or changing authentication, authorization, data handling, APIs, dependencies, infrastructure, or other security-sensitive behavior.

Do not place secrets, personal data, or exploitable vulnerability details in public issues or pull requests.

## 1. Scope and threat modeling

- [ ] Assets and sensitive data are identified.
- [ ] Entry points, trust boundaries, and data flows are documented.
- [ ] Relevant threats and abuse cases are considered.
- [ ] Attack surface and external dependencies are identified.
- [ ] Security requirements and risk severity are recorded.
- [ ] High-risk assumptions have been validated.

## 2. Identity and access control

- [ ] Authentication is required for protected operations.
- [ ] Authorization is checked server-side for every protected resource/action.
- [ ] Access control follows least privilege and deny-by-default principles.
- [ ] Resource ownership and tenant boundaries are enforced.
- [ ] Privilege escalation and insecure direct object reference scenarios are tested.
- [ ] Session/token expiration, rotation, revocation, and storage are appropriate.
- [ ] Passwords use a modern password-hashing algorithm and appropriate parameters.
- [ ] Multi-factor authentication is considered for privileged or sensitive accounts.
- [ ] Administrative actions are restricted and auditable.

## 3. Application and API security

- [ ] All untrusted input is validated using explicit schemas or equivalent controls.
- [ ] Output is encoded appropriately to prevent injection.
- [ ] Database queries use safe parameterization or safe query builders.
- [ ] Cross-site scripting, CSRF, SSRF, and injection risks are assessed as applicable.
- [ ] CORS, security headers, and content security policy are configured appropriately.
- [ ] Rate limiting and abuse protection cover sensitive endpoints.
- [ ] File uploads validate type, size, content, and storage location.
- [ ] File access is authorized; private files are not exposed through predictable public URLs.
- [ ] Redirects, URL fetches, and archive extraction are protected against abuse.
- [ ] Error responses do not expose stack traces, secrets, or internal implementation details.

## 4. Data protection and privacy

- [ ] Only necessary personal and sensitive data is collected.
- [ ] Data is classified and handled according to its sensitivity.
- [ ] Transport encryption is enabled for sensitive communications.
- [ ] Sensitive stored data is encrypted where appropriate.
- [ ] Secrets and credentials are not committed to source control or logs.
- [ ] Retention, deletion, export, and backup handling are defined.
- [ ] Logs avoid tokens, passwords, and unnecessary personal data.
- [ ] Access to sensitive data is logged where required.
- [ ] Privacy and regulatory obligations have been reviewed.

## 5. Dependencies and software supply chain

- [ ] Dependencies come from trusted sources.
- [ ] Dependency versions are pinned or constrained appropriately.
- [ ] Vulnerability scanning is enabled where available.
- [ ] Unmaintained or unnecessary dependencies are removed.
- [ ] Build scripts and lifecycle hooks are reviewed for risk.
- [ ] Lockfiles are committed and changes are reviewed.
- [ ] CI/CD credentials use least privilege and are protected.
- [ ] Build artifacts and release provenance are controlled where required.

## 6. Infrastructure and deployment

- [ ] Production configuration is separated from development configuration.
- [ ] Secrets are injected through an approved secret-management mechanism.
- [ ] Network exposure is minimized.
- [ ] Service and database accounts have minimum required permissions.
- [ ] Storage buckets, object stores, and backups are not unintentionally public.
- [ ] TLS certificates and key rotation are managed.
- [ ] Administrative interfaces are protected.
- [ ] Infrastructure changes are reviewed and auditable.

## 7. Detection and response

- [ ] Security-relevant events are logged without exposing secrets.
- [ ] Alerts exist for important suspicious activity.
- [ ] Logs are access-controlled and retained appropriately.
- [ ] Incident ownership and escalation paths are known.
- [ ] A process exists to revoke credentials and contain compromised components.
- [ ] Backup restoration and incident recovery have been considered.

## Findings and disposition

For each finding, record:

| Finding | Severity | Owner | Mitigation | Due date | Status |
|---|---|---|---|---|---|
| | | | | | |

**Overall risk:** Low / Medium / High / Critical

**Decision:** Approved / Approved with actions / Blocked

**Reviewer and date:**

**Exceptions accepted by (name/role):**

**Evidence links:** threat model, test results, scan reports, configuration review, and relevant tickets.
