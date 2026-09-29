# Security and Threat Model

## Reporting

Until a dedicated security contact and private reporting channel are published, do not submit secrets, personal victim data, exploit details, or live credentials to public issues.

## Protected properties

The protocol aims to protect human authorization, member identity where privacy is appropriate, request confidentiality, integrity of Charters and Manifests, resource limits, revocation, auditability, and service continuity.

## Primary threats

- Sybil members and fabricated quorum
- Compromised or malicious agents and Operators
- Forged, replayed, or stale delegations and beacons
- Membership-graph enumeration and cross-network tracking
- Prompt injection and malicious evidence
- Privilege expansion through agent-to-agent delegation
- Resource exhaustion and beacon storms
- Correlated relay, cloud, or governance failure
- False capability claims and reputation manipulation
- Insider access to victim information
- Split-brain governance and conflicting Charter versions
- Supply-chain compromise

## Baseline controls

- signed, expiring artifacts and proof of key possession;
- key rotation, revocation, and recovery procedures;
- least privilege and deny-by-default authorization;
- independent review for high-impact actions;
- rate limits, budgets, leases, idempotency, and stop conditions;
- encryption in transit and at rest where appropriate;
- data minimization and bounded retention;
- failure-domain diversity for quorum and recovery;
- tamper-evident logs with access control;
- routine adversarial testing and public disclosure of known limitations.

## Non-goals

No protocol can guarantee availability under every attack, validate every human claim, eliminate operator compromise, or make an unsafe agent safe merely through membership. Implementations must publish their assumptions and residual risks.
