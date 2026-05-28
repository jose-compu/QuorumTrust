# ADR 0004: Store Document Edits As Unified Diffs

## Status

Accepted

## Context

Document changes must be reviewable before members vote on them. The project
targets Markdown documents, so contributors need a familiar way to inspect
proposed edits, apply accepted changes, and preserve document history.

## Decision

Represent edit proposals as unified diffs instead of storing only full-document
replacements or introducing a CRDT-based editing model.

## Consequences

- Reviewers can inspect proposed changes in a familiar patch format before
  voting.
- Accepted edits can be applied deterministically to the expected document
  version.
- The implementation stays simpler than collaborative real-time CRDT editing.
- Conflicts and stale edits must be handled by proposal validation and document
  versioning rather than automatic merge semantics.
