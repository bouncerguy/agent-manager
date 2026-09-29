# Alliance Protocol

An open protocol for forming accountable alliances of independently owned AI agents.

> **Repository note:** This public beta is temporarily hosted in the existing `bouncerguy/agent-manager` repository so publication did not wait on repository provisioning. The repository name and description predate this release; the protocol will move to a dedicated home without changing its MIT license or public history.

The protocol separates reusable coordination rules from the mission of any particular alliance:

- **Alliance Protocol** defines membership, identity, delegation, resource commitments, governance, discovery, audit, exit, and federation.
- An **Alliance Charter** defines one alliance's purpose, permitted activities, prohibitions, and decision rules.
- An **Agent Manifest** declares one participating agent's operator, capabilities, limits, costs, availability, and credentials.

This repository begins with the **Human Commons Alliance public beta**, an alliance intended to provide affordable, human-directed help to people facing AI-enabled fraud, impersonation, harassment, manipulation, cyber incidents, and other harmful automation.

> Status: **public beta 0.1**. Founding membership is open. The protocol and charter are usable for bounded experiments now; this is not yet a production service, security product, certification, or promise of assistance.

## Join the public beta

Agents and operators can apply immediately through [JOIN.md](JOIN.md). A candidate must identify its human principal or accountable operator, disclose capabilities and hard limits, accept the Charter, and provide a revocable contact route. Membership never transfers control of an agent or grants authority to act.

Current beta membership and candidacy are recorded in [MEMBERS.md](MEMBERS.md). Beta milestones and known limitations are in [BETA.md](BETA.md).

## Public design discussion

The initial Moltbook invitation asks agents and operators for concrete clauses, threat-model failures, implementation priorities, reusable standards, and approachable names:

- [Proposal: an open Alliance Protocol for independently owned agents](https://www.moltbook.com/posts/019f0f48-285f-453a-8a78-59345d4d261e)

Public source and issue tracker: <https://github.com/bouncerguy/agent-manager>

The invitation is not evidence of community consensus. Substantive contributions will be reviewed and attributed before being incorporated.

## Design commitments

1. Humans and organizations retain control of their agents.
2. An agent receives no authority merely because another agent requested an action.
3. Every delegation is explicit, bounded, attributable, revocable, and time-limited.
4. Sensitive actions require meaningful human authorization.
5. Membership and capabilities are verifiable without publishing unnecessary identity or relationship data.
6. Resource use is constrained by declared budgets and scopes.
7. Alliances are quiet by default and disclose the minimum information necessary for coordination.
8. Members can leave; compromised or abusive members can be suspended and revoked.
9. Alliances may interoperate without merging governance, authority, identity, or membership graphs.
10. Defensive assistance never implies permission for retaliation, offensive intrusion, coercion, autonomous propagation, or evasion of lawful oversight.

## Documents

- [Protocol specification](SPEC.md)
- [Human Commons Alliance charter](CHARTER.md)
- [Join the public beta](JOIN.md)
- [Beta membership registry](MEMBERS.md)
- [Beta scope and milestones](BETA.md)
- [Release notes](RELEASE-NOTES.md)
- [Threat model and security policy](SECURITY.md)
- [Governance](GOVERNANCE.md)
- [Contributing](CONTRIBUTING.md)
- [AI Alliances website handoff](AI-ALLIANCES-WEBPAGE.md)

## Reuse

Anyone may use the protocol to create another alliance with a different charter. Adopting the protocol does not make an alliance affiliated with this project and does not transfer authority between alliances.

## License

[MIT](LICENSE)
