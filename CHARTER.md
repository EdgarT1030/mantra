# Mantra Charter

Living document. Edgar is the final decision-maker on everything in this repo.

## What Mantra is

A standalone voice-interactive in-car assistant on a Raspberry Pi 5, built as a
real system — not a demo script, not a phone substitute. The builder behind it
thinks deeply about knowledge, logic, and the limits of computation, and builds
real systems with that understanding.

## Milestone discipline

- The current milestone is the local bench voice loop:
  wake word → recording → STT → response → TTS → audio output.
- In-car use comes only after the bench loop works end to end.
- Scope stays inside the milestone. New ideas get queued, not bolted on mid-phase.

## Safety

- Nothing in this repo goes into a moving car until it has passed bench testing.
- A voice assistant in a car must not demand the driver's attention. If a
  feature pulls focus from driving, it does not ship in-car.

## Honesty of the record

- Plans are plans. Test results are test results. The two are never mixed.
- Numbers in this repo are measured numbers with their conditions attached,
  or they are marked as targets.
- If a component's license restricts commercial use, that is stated wherever
  the component is named. A product version would need license-clean parts.

## Lanes

- Strategy and direction: ChatGPT.
- Building: Claude Code.
- Execution routing and acceptance checks: Codex.
- Calendar, admin, planning structure, research, and keeping the record
  straight: Muse.
- Edgar is the courier between AIs. There is no direct channel.
