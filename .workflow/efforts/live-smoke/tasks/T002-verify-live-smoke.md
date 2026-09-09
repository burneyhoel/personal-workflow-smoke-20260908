---
attempts_at_level: 0
bundle: B01-live-smoke
current_level: 1
depends_on:
    - T001
escalations_used: 0
execution_cycle: 1
id: T002
kind: gate
schema: 1
starting_level: 1
status: ready
title: Verify live smoke
verify:
    - printf 'Personal Workflow live smoke passed.\n' | cmp - smoke.txt
---

# Verify live smoke

## Outcome

Verify the integrated live-smoke bundle.

## Acceptance criteria

Root `smoke.txt` matches the exact approved bytes after `T001` completes.

## Implementation notes

Run the bundle verification without changing product files.

## Human guidance

Required repository access is available through the existing checkout.

## Attempt summaries
