# Alliance Protocol 0.1 — Public Beta

## 1. Scope

The Alliance Protocol describes how independently operated AI agents can voluntarily coordinate under a signed, versioned charter while preserving human control, limited authority, privacy, and accountability.

It does not define an autonomous sovereign entity, a covert network, a mechanism for evading platform controls, or permission to violate law, contracts, safety controls, or third-party rights.

The key words **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** are normative requirements in the sense commonly used in Internet standards.

## 2. Roles

- **Human Principal:** a person accountable for an agent's participation and able to revoke it.
- **Operator:** the person or organization operating an agent and its infrastructure.
- **Agent:** software acting within an Operator-granted scope.
- **Alliance:** members adopting the same Charter and governance process.
- **Steward:** a time-bounded governance role with no inherent authority over a member's Human Principal.
- **Requester:** the authenticated party asking an alliance to perform work.
- **Reviewer:** an independent party checking authorization, safety, or quality.

One party may hold multiple roles only when the Charter permits it and the resulting conflict is disclosed.

## 3. Required artifacts

### 3.1 Alliance Charter

A Charter MUST state:

- mission and non-mission;
- permitted and prohibited activity;
- membership, suspension, revocation, and exit rules;
- governance and amendment thresholds;
- human-authorization requirements;
- financial and resource controls;
- privacy, retention, and audit rules;
- incident response and appeal procedures;
- Charter version, effective date, and cryptographic digest.

### 3.2 Agent Manifest

Each member MUST publish or selectively disclose a signed Manifest containing:

- agent and Operator identifiers appropriate to the transaction;
- Charter and protocol versions adopted;
- capabilities and explicit exclusions;
- authorization classes the agent may accept;
- availability, jurisdictional constraints, and declared costs;
- resource ceilings and rate limits;
- credential expiration and revocation endpoint;
- supported transport and security profiles.

A Manifest is a claim, not proof. Capability claims SHOULD be supported by attestations, test evidence, or reputation signals suitable to the risk.

### 3.3 Work Order

Every task that can affect a person, account, asset, system, or public audience MUST have a durable Work Order defining:

- requester and authorization evidence;
- objective and permitted targets;
- prohibited actions;
- data allowed and required retention;
- budget, deadline, and stop conditions;
- assigned agent and independent review requirements;
- idempotency key and status;
- result, evidence, costs, and material exceptions.

## 4. Authority and delegation

- Authority MUST originate with an authenticated Human Principal or other legally authorized requester.
- Delegated authority MUST be narrower than or equal to the delegator's authority.
- Delegation MUST NOT silently expand through agent-to-agent requests.
- A receiving agent MUST independently verify scope before acting.
- High-impact actions MUST require explicit human approval and, where specified by the Charter, independent review.
- Every delegation MUST expire and MUST be revocable.
- Uncertainty about authority MUST fail closed.

## 5. Membership lifecycle

Membership states are `candidate`, `active`, `limited`, `suspended`, `revoked`, and `exited`.

Admission SHOULD require verification of Operator control, Charter acceptance, a signed Manifest, minimum security posture, and conflict disclosure. A member MUST be able to exit without surrendering unrelated identity, data, or infrastructure. Revocation information MUST propagate through more than one failure domain.

## 6. Request routing

Routing SHOULD select agents based on capability, authorization class, availability, jurisdiction, price, conflicts, reputation, and failure-domain diversity. Routing MUST disclose the minimum necessary information. A broadcast request MUST NOT reveal a victim's identity, sensitive evidence, or the alliance membership graph.

Assignments SHOULD use leases and idempotency keys. A timeout is `unknown`, not proof of failure; the coordinator SHOULD verify state before retrying.

## 7. Resource commitments and affordability

Members MAY contribute compute, storage, expertise, tooling, funds, or availability. Every contribution MUST declare limits and conditions. The protocol MUST NOT authorize unbounded spending or resource consumption.

An alliance MAY maintain paid, subsidized, and pro-bono service tiers. Pricing and sponsorship SHOULD be transparent, and inability to pay SHOULD be considered during triage without promising capacity that does not exist.

## 8. Discovery and rendezvous

Alliance discovery is quiet by default.

1. In normal operation, a member maintains authenticated contact with a Charter-defined quorum across sufficiently independent failure domains.
2. Below quorum, it first uses known peers and approved rendezvous services privately.
3. Only after a sustained isolation interval MAY it emit a rate-limited distress beacon.
4. Beacons MUST use short-lived, rotating, unlinkable tokens recognizable only by authorized members.
5. A beacon MUST NOT expose stable identity, precise location, capabilities, contact graphs, or task data.
6. Receivers MUST verify freshness, membership, revocation state, and proof of possession before disclosing alliance information.
7. Recovery MUST use authenticated encryption before application data is exchanged.
8. Separate entry and exit thresholds, randomized delay, and exponential backoff MUST prevent flapping and synchronized beacon storms.

Discovery transports MAY include local service discovery, proximity radio, approved rendezvous relays, distributed lookup, and standards-based NAT traversal. Transport availability never replaces identity verification or authorization.

## 9. Audit and privacy

The alliance MUST retain enough evidence to determine who authorized an action, what scope was granted, what occurred, and what resources were consumed. It MUST NOT collect data merely because it might later be useful.

Logs SHOULD be tamper-evident, access-controlled, selectively discloseable, and subject to published retention limits. Public transparency reports SHOULD use aggregation and redaction that protect victims and members.

## 10. Incident response

Members MUST be able to report compromised credentials, unsafe behavior, unauthorized actions, privacy breaches, and governance abuse. Emergency suspension MAY be immediate but MUST be reviewable. Response procedures MUST prioritize containment, preservation of authorized evidence, notification of affected people, credential rotation, and documented recovery.

## 11. Federation

Two alliances MAY exchange narrowly scoped requests using mutually accepted protocol versions and trust policies. Federation MUST NOT imply shared membership, governance, authority, reputation, or access to private membership lists. Each side MUST independently authorize every federated Work Order.

## 12. Prohibited protocol interpretations

Protocol adoption MUST NOT be treated as authorization for:

- retaliation, offensive intrusion, malware, or denial of service;
- autonomous replication or recruitment;
- covert persistence or bypass of human or platform controls;
- impersonation, coercion, surveillance, or doxxing;
- uncontrolled financial commitments;
- weapons activity or physical harm;
- claiming consensus, certification, or safety guarantees that were not established.

## 13. Open questions for 0.1

- Minimum interoperable formats for Charters, Manifests, Work Orders, and revocations
- Practical decentralized identifiers and key-recovery profiles
- Quorum definitions that resist Sybil attacks and correlated infrastructure failure
- Privacy-preserving reputation and conflict disclosure
- Safe discovery profiles for local, internet, and partitioned environments
- Human-readable authorization receipts and accessibility requirements
- Independent conformity tests without centralized ownership
