# Mantra bench test plan

For the local bench voice loop: wake word → recording → STT → response →
TTS → audio output. Every run gets a log in `docs/test-logs/` named
`YYYY-MM-DD-<what-was-tested>.md`.

## Setup

- Quiet room, Pi 5 on the bench, ReSpeaker mic array connected, DAC + speaker
  connected.
- One tester speaking at normal volume, about an arm's length from the mic.
- Note Pi software versions and the test phrase list before starting.

## Procedure

1. Say the wake word. Record: did the loop start? How many tries?
2. Speak a test phrase. Record the STT transcript exactly, and whether it
   matches what was said.
3. Check the response: is it sensible given the transcript?
4. Listen to the TTS output: is every word intelligible at bench distance?
5. Repeat steps 1–4 with at least five different phrases, including one with
   background noise (music or a fan on low).
6. Run the whole loop hands-free three times in a row with no restarts.

## Pass criteria

- The loop starts on the wake word in a quiet room without repeated shouting.
- Transcripts match the spoken phrases (log every miss verbatim).
- Responses make sense given the transcripts.
- TTS output is intelligible at bench distance.
- Three consecutive hands-free runs complete with no manual restart.

## Log template

```markdown
# Test log — YYYY-MM-DD — <what was tested>

- Hardware/software versions:
- Test phrases:
- Wake word attempts / successes:
- Transcript results (exact, including misses):
- Response notes:
- TTS intelligibility notes:
- Pass / fail per criterion:
- Next fix:
```
