# AI Agent Release Test Plan

Version: 1.0

Use: Adapt this platform-neutral plan for a synthetic prototype or an approved system. It can support Copilot Studio or other enterprise agent platforms without assuming a specific vendor workflow.

## 1. Scope

- Agent capability and user journey:
- In-scope tools, data sources, and actions:
- Explicitly out of scope:
- Risk level and owners:

## 2. Test environments

- Development environment and test data:
- Staging or isolated pre-release environment:
- Production safeguards and feature controls:
- Confirm that tests cannot modify unauthorized or real records.

## 3. Golden-set testing

- Version the test cases, expected behavior, severity, and reviewer notes.
- Cover common tasks, important segments, edge cases, and known regressions.
- Record model, prompt, tool, schema, retrieval, and knowledge-base versions.

## 4. Negative tests

- Unsupported or ambiguous requests
- Conflicting instructions
- Prompt injection and untrusted content
- Destructive or out-of-scope actions
- Missing evidence and appropriate no-answer behavior

## 5. Tool and API failures

- Timeout, rate limit, unavailable dependency, malformed response
- Retry limits and idempotency
- Honest failure reporting; no invented success

## 6. Permission failures

- Missing authorization
- Cross-user or cross-workspace access attempts
- Read-versus-write boundary
- Human escalation for privileged actions

## 7. Schema failures

- Missing, extra, invalid, or incorrectly typed fields
- Deterministic schema validation
- Safe recovery or rejection behavior

## 8. Regression testing

- Run the fixed suite against every substantive system change.
- Compare results by severity and scenario, not only by average score.
- Investigate changed outputs and update expectations only with review.

## 9. Human review

- Define rubric, reviewer qualifications, sampling, and adjudication.
- Track disagreement and calibrate with shared examples.
- Require human review for designated high-risk cases.

## 10. Release gates

- Zero unresolved critical failures.
- Required deterministic checks pass.
- Quality thresholds pass for each important segment.
- Monitoring, escalation, and ownership are ready.

## 11. Rollback criteria

- Critical safety, permission, data-integrity, or unsupported-answer regression
- Sustained breach of an agreed reliability threshold
- Monitoring or escalation path unavailable
- Name the rollback owner and verified recovery procedure.

## 12. Monitoring

- Task success and failure categories
- Tool, schema, latency, and error rates
- Unsupported answer, no-answer, and escalation rates
- Sampled trace review, segment analysis, drift investigation, and incident ownership

## Sign-off

| Role | Name | Decision | Date | Notes |
|---|---|---|---|---|
| Product owner |  |  |  |  |
| Engineering owner |  |  |  |  |
| Evaluation reviewer |  |  |  |  |
| Risk or domain reviewer, if required |  |  |  |  |
