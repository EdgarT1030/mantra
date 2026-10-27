# Mantra

Mantra is a standalone voice-interactive in-car assistant built on a Raspberry Pi 5.
It is a bench project first: the current milestone is a local bench voice loop that
runs entirely on the bench before anything goes near a car.

## The loop

```
wake word → recording → STT → response → TTS → audio output
```

Status: on the bench, not in the car yet.

## Hardware in hand

- Raspberry Pi 5 board + Active Cooler
- ReSpeaker mic array
- OBDLink EX
- DAC

Still outstanding: the SSD kit (a 64 GB microSD boots everything, so nothing is
blocked). Full inventory and status: see `docs/HARDWARE.md`.

## Repo map

- `docs/BUILD_PLAN.md` — the phased build plan, from bench setup to loop integration
- `docs/HARDWARE.md` — parts inventory and status
- `docs/TEST_PLAN.md` — how the bench voice loop gets tested
- `CHARTER.md` — what this project is and the rules it runs by
- `AGENTS.md` — working notes for the AIs helping on this build

## Rules of the season

1. Bench loop first, in-car use later. No install step jumps the queue.
2. A step is done only when bench evidence says so — no claims from plans alone.
3. Any future product version needs license-clean parts; some current candidate
   components carry noncommercial licenses.
