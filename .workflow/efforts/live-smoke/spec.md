---
schema: 1
status: approved
decision_promotion: not-needed
---

# Live smoke

## Problem

The live smoke effort lost its temporary checkout and needs a durable specification for the approved smoke-file change.

## Desired outcome

The repository root contains `smoke.txt` with the exact approved bytes and no other product changes.

## Observable requirements

- Create `smoke.txt` at the repository root.
- The file content is exactly `Personal Workflow live smoke passed.` followed by one LF.
- The implementation changes no other product file.

## Constraints and decisions

- Treat the required content as bytes. Do not add a BOM, extra whitespace, or another line ending.
- Limit product scope to root `smoke.txt`.
- No project-wide decision documentation is needed.

## Acceptance scenarios

- Reading root `smoke.txt` as bytes returns `Personal Workflow live smoke passed.\n`.
- Comparing product changes against the implementation base shows only root `smoke.txt`.

## Out of scope

Any product change other than creating root `smoke.txt` with the required bytes.

## Open questions

None.
