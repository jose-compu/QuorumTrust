# ADR 0002: Require Greater Than Two-Thirds Governance Approval

## Status

Accepted

## Context

Membership changes and document lifecycle actions affect the authority of the
network. A simple majority could let a small coalition push through changes in a
split network, while unanimous approval would make routine collaboration fragile.

## Decision

Require greater than two-thirds approval from active members for governance
actions, including membership changes, document edits, finalization, and member
expulsion.

## Consequences

- Accepted proposals represent broad agreement from the current active member
  set.
- The network tolerates some unavailable or dissenting members while still
  allowing progress.
- Proposal status depends on an accurate active-member view across nodes.
- Small networks have coarse thresholds; for example, a two-member network needs
  both members to approve because one vote is not greater than two-thirds.
