---
attempts_at_level: 0
bundle: B01-live-smoke
current_level: 2
depends_on: []
escalations_used: 0
execution_cycle: 1
id: T001
kind: task
schema: 1
starting_level: 2
status: ready
title: Create smoke file
verify:
    - printf 'Personal Workflow live smoke passed.\n' | cmp - smoke.txt
---

# Create smoke file

## Outcome

Create root `smoke.txt` with the exact approved bytes.

## Acceptance criteria

Root `smoke.txt` contains exactly `Personal Workflow live smoke passed.` followed by one LF, with no other product changes.

## Implementation notes

Limit the product change to root `smoke.txt` as specified in `.workflow/efforts/live-smoke/spec.md`.

## Human guidance

Required repository access is available through the existing checkout.

## Attempt summaries
