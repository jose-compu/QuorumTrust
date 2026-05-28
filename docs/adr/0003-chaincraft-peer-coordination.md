# ADR 0003: Use Chaincraft For Peer Coordination

## Status

Accepted

## Context

QuorumTrust needs peer-to-peer message propagation for proposals, votes,
governance sync, and FROST signing messages. The project should avoid a central
coordinator while still reusing an existing decentralized networking layer.

## Decision

Use Chaincraft as the peer coordination and gossip layer. QuorumTrust defines its
own governance, document, and FROST messages on top of that networking layer.

## Consequences

- QuorumTrust can focus on governance and document semantics instead of building
  a full P2P transport from scratch.
- Message validation and state convergence remain QuorumTrust responsibilities.
- Runtime behavior depends on Chaincraft's networking guarantees and operational
  configuration.
- Future networking changes should preserve the same high-level message model so
  governance and signing logic stay isolated from transport details.
