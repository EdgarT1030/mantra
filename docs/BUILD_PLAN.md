# Mantra build plan

Milestone: a local bench voice loop on the Raspberry Pi 5 —
wake word → recording → STT → response → TTS → audio output.
In-car install is a later season, not part of this plan.

## Phase 0 — Bench setup

- [ ] Inventory every part against `docs/HARDWARE.md`.
- [ ] Boot the Pi 5 from microSD (64 GB boots everything; the SSD kit is not
      a blocker).
- [ ] Confirm the ReSpeaker mic array captures clean audio and the DAC drives
      a speaker.
- [ ] Set up the repo working environment (Python venv, git, docs folders).
- Exit: Pi boots, mic records, speaker plays, all on the bench.

## Phase 1 — Wake word

- [ ] Pick the wake-word approach (openWakeWord custom classifier is the
      leading candidate on file).
- [ ] Train the classifier: synthesize positives with a TTS voice matched to
      the real pronunciation, feed 80 ms windows, and sweep the detection
      threshold to measure recall.
- [ ] Fine-tune with real recordings (tens of samples, not thousands).
- Exit: the bench Pi reliably wakes on the chosen word in a quiet room, with
  the measured recall logged.

## Phase 2 — Recording + STT

- [ ] Capture microphone audio cleanly from the ReSpeaker array after wake.
- [ ] Evaluate local STT candidates on the Pi 5 for accuracy and latency.
- [ ] Pick on bench numbers, not on reputation.
- Exit: spoken test phrases come back as accurate transcripts, logged.

## Phase 3 — Response

- [ ] Define what "response" means for the bench loop: a spoken answer to a
      spoken prompt, produced locally or by a documented service call.
- [ ] The local-vs-cloud response decision is open and must be recorded with
      its reasons (latency, privacy, cost, license) before it is built on.
- Exit: a transcript in produces a sensible spoken answer out, end to end.

## Phase 4 — TTS + audio output

- [ ] Pick a TTS voice and route it through the DAC to a speaker.
- [ ] Check intelligibility at normal bench distance and over background noise.
- Exit: answers are clearly audible from the bench speaker.

## Phase 5 — Loop integration + bench test

- [ ] Wire all five stages into one hands-free loop.
- [ ] Run the full procedure in `docs/TEST_PLAN.md` and log the results.
- Exit: the milestone is met when the loop runs hands-free, repeatedly, with
  a written test log — not when the code merely exists.

## Later (not this season)

- In-car install and power (UPS, ignition behavior).
- OBDLink EX vehicle data.
- Any product, investor, or Y Combinator version — that needs license-clean
  parts and is a separate decision.
