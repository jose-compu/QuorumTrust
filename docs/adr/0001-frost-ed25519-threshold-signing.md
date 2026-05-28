# ADR 0001: Use FROST Ed25519-SHA512 For Threshold Signing

## Status

Accepted

## Context

QuorumTrust needs members to finalize documents without giving any single node
authority to sign on behalf of the group. The signing scheme must support
threshold participation, produce signatures that are easy to verify, and fit the
project's Rust implementation.

## Decision

Use FROST Ed25519-SHA512 threshold signatures through the Thetacrypt primitives.
Final document signatures are assembled only after the required governance vote
has passed, and member identities are based on Ed25519 public keys.

## Consequences

- No individual node can unilaterally produce a final group signature.
- Finalized documents can carry a compact Ed25519-compatible signature.
- Nodes must coordinate FROST key-share distribution, nonce commitments, partial
  signatures, and final signature assembly.
- Recovery and key rotation flows need explicit protocol support because signing
  state depends on the active threshold member set.
