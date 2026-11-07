# Production Readiness Review

Use this checklist before releasing a new production service or a material change that affects reliability, security, data, or operations.

A checked item should have evidence. Record justified exceptions with an owner and target date.

## 1. Ownership and support

- [ ] A service owner and technical contact are identified.
- [ ] Support hours and escalation paths are documented.
- [ ] Dependencies and their owners are known.
- [ ] Service-level objectives or operational expectations are defined where appropriate.
- [ ] Known limitations and operational risks are documented.

## 2. Build and configuration

- [ ] Build and deployment are reproducible.
- [ ] Environments are separated and configured consistently.
- [ ] Configuration is validated at startup.
- [ ] Secrets are managed outside source control.
- [ ] Runtime and dependency versions are supported.
- [ ] CI checks and required tests pass.
- [ ] Production debug modes and development credentials are disabled.

## 3. Data and state

- [ ] Database migrations are reviewed and tested.
- [ ] Migrations are safe for the deployment sequence and expected data volume.
- [ ] Backup schedules and retention are configured.
- [ ] Restore procedures have been tested at an appropriate level.
- [ ] Data retention and deletion behavior are understood.
- [ ] Cache, queue, and object-storage behavior is documented.
- [ ] Data integrity checks exist for critical workflows.

## 4. Reliability and capacity

- [ ] Resource requirements and capacity assumptions are documented.
- [ ] Timeouts are configured for network and database operations.
- [ ] Retries use bounded attempts and appropriate backoff.
- [ ] Idempotency is implemented for operations that may be retried.
- [ ] Queue sizes and concurrency are bounded where applicable.
- [ ] Health and readiness checks are available.
- [ ] Graceful shutdown and in-flight work handling are addressed.
- [ ] Critical dependency failure behavior is understood.
- [ ] Load or performance testing is completed when warranted.

## 5. Observability

- [ ] Structured logs include useful context and correlation identifiers.
- [ ] Logs exclude secrets and unnecessary sensitive data.
- [ ] Key business and technical metrics are available.
- [ ] Distributed traces are available where useful.
- [ ] Dashboards cover health, traffic, errors, and saturation.
- [ ] Alerts have clear thresholds, owners, and response guidance.
- [ ] Error rates and latency can be investigated by endpoint or operation.

## 6. Security and compliance

- [ ] Authentication and authorization are verified in production configuration.
- [ ] Network access and infrastructure permissions follow least privilege.
- [ ] TLS and secure transport are configured.
- [ ] Security headers and relevant platform protections are enabled.
- [ ] Dependency and container/image scans are reviewed where applicable.
- [ ] Audit logging is enabled for sensitive operations where required.
- [ ] Privacy, retention, and regulatory obligations are addressed.
- [ ] No known critical or unaccepted high-severity security findings remain.

## 7. Deployment and rollback

- [ ] Deployment steps are documented and repeatable.
- [ ] Release artifacts are identifiable and traceable to source revisions.
- [ ] Rollback or roll-forward strategy is documented.
- [ ] Database and data changes have a recovery strategy.
- [ ] Feature flags or staged rollout are used when appropriate.
- [ ] Smoke tests verify critical user journeys after deployment.
- [ ] Deployment ownership and communication are clear.

## 8. Operational readiness

- [ ] Runbooks cover common failures and routine operations.
- [ ] On-call/support personnel know how to diagnose key failure modes.
- [ ] Incident response and escalation procedures are known.
- [ ] Capacity, quotas, and cost are monitored.
- [ ] Third-party service limits and failure behavior are understood.
- [ ] Maintenance and patching responsibilities are assigned.
- [ ] User-facing status or communication process exists where needed.

## Go / no-go decision

**Decision:** Go / Go with accepted actions / No-go

**Release/version:**

**Service owner:**

**Review date:**

**Known risks and accepted exceptions:**

| Action | Risk | Owner | Due date | Tracking link |
|---|---|---|---|---|
| | | | | |

**Approvals:**
- Engineering:
- Security (if required):
- Operations (if required):
- Product/business owner (if required):
