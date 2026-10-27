# AGENTS.md — working notes for Mantra

## How to work in this repo

- Docs before code claims. If it is not written down here, it did not happen.
- Every build phase ends with a bench test from `docs/TEST_PLAN.md`. A phase
  without a test log is not finished.
- Keep files small and plain. No resume-speak, no corporate filler, no
  impressive-sounding text that says nothing.
- Do not rename the project, change the milestone, or add a phase without
  Edgar's word.

## Conventions

- Hardware status lives in exactly one place: `docs/HARDWARE.md`. Update it
  there when a part arrives or a plan changes; do not scatter status notes
  across other files.
- Test logs go in `docs/test-logs/` with the date in the filename
  (`YYYY-MM-DD-<what-was-tested>.md`).
- Benchmarks record hardware, software versions, conditions, and the raw
  numbers. A number without conditions is not a result.

## What not to do

- Do not claim in-car readiness. The milestone is the bench loop.
- Do not present a plan as a result.
- Do not add a dependency, a part, or a service without saying what it is
  for and what it costs (money, latency, or license terms).
