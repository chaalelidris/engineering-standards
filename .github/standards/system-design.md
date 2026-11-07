# System Design Review

Use this checklist for new systems and material changes to architecture, data flows, integrations, or service boundaries. Tailor the depth of review to the change's risk.

## 1. Problem and requirements

- [ ] The problem, users, and expected outcomes are clearly stated.
- [ ] Functional requirements and explicit non-goals are documented.
- [ ] Quality attributes are identified (availability, latency, throughput, consistency, durability, privacy, accessibility, and cost).
- [ ] Expected workload is estimated: users, requests, data volume, growth, and peak patterns.
- [ ] Constraints and assumptions are recorded.
- [ ] Acceptance criteria are measurable and testable.

## 2. Architecture and boundaries

- [ ] A current or proposed architecture diagram exists where useful.
- [ ] Responsibilities and ownership of components are clear.
- [ ] Service/module boundaries minimize unnecessary coupling.
- [ ] Synchronous and asynchronous interactions are chosen deliberately.
- [ ] External dependencies, failure modes, and ownership are documented.
- [ ] Architecture decisions and significant trade-offs are recorded.
- [ ] The design avoids unnecessary complexity and premature distribution.

## 3. Data and persistence

- [ ] Data entities, relationships, ownership, and lifecycle are defined.
- [ ] Data consistency and transaction boundaries are understood.
- [ ] Indexes, query patterns, and expected data growth are considered.
- [ ] Retention, deletion, archival, and backup requirements are defined.
- [ ] Schema changes and migration/rollback strategies are safe.
- [ ] Sensitive data is classified and minimized.
- [ ] Cache invalidation, expiration, and consistency behavior are defined where applicable.

## 4. API and integration contracts

- [ ] API contracts, validation rules, and error semantics are documented.
- [ ] Authentication and authorization are enforced at the appropriate boundary.
- [ ] Pagination, filtering, sorting, and rate limits are considered where relevant.
- [ ] Compatibility and versioning strategy is clear.
- [ ] Timeouts, retries, backoff, and idempotency are designed for remote calls.
- [ ] Webhooks/events are authenticated and protected against replay where applicable.
- [ ] Integration failures are observable and recoverable.

## 5. Reliability and scalability

- [ ] Single points of failure are identified.
- [ ] Capacity limits and bottlenecks are considered.
- [ ] Load shedding, backpressure, and queue limits are considered where relevant.
- [ ] Retry behavior cannot create retry storms or duplicate side effects.
- [ ] Critical operations have defined timeout and failure behavior.
- [ ] Availability and recovery objectives are stated where required.
- [ ] Graceful degradation and dependency outage behavior are defined.

## 6. Security and privacy

- [ ] Threats and trust boundaries have been considered.
- [ ] Least privilege is applied to users, services, and infrastructure.
- [ ] Secrets are stored and rotated securely.
- [ ] Input validation and output encoding are applied at trust boundaries.
- [ ] Sensitive data is protected in transit and at rest as appropriate.
- [ ] Audit requirements and security-relevant events are identified.
- [ ] Privacy, consent, retention, and data residency obligations are considered.

See the [Security Review Checklist](security-checklist.md) for a deeper review.

## 7. Operability

- [ ] Logs, metrics, and traces support diagnosis.
- [ ] Health checks distinguish liveness from readiness where applicable.
- [ ] Alerts are actionable and have an owner.
- [ ] Operational dashboards and runbooks exist for critical paths.
- [ ] Deployment, rollback, and migration procedures are documented.
- [ ] Resource usage and operating costs are estimated.
- [ ] Support ownership and escalation paths are clear.

## 8. Verification

- [ ] Unit, integration, and end-to-end test boundaries are defined.
- [ ] Performance and load testing are planned when warranted.
- [ ] Failure scenarios and recovery paths are tested.
- [ ] Security testing is proportionate to risk.
- [ ] Migration and backward-compatibility tests are included where needed.
- [ ] Acceptance criteria can be verified before release.

## Review outcome

**Decision:** Approved / Approved with actions / Needs revision

**Reviewers:**

**Date:**

**Key risks and trade-offs:**

**Required actions (owner, due date, evidence):**

---

## Architecture Decision Record (ADR) starter

For significant decisions, record:

- **Title:** concise decision name
- **Status:** proposed / accepted / superseded / rejected
- **Context:** problem, constraints, and forces
- **Decision:** selected approach
- **Alternatives:** options considered
- **Consequences:** benefits, costs, risks, and follow-up work
