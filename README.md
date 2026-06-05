# OmegaClaw — Operational Evidence Supplement

Supplementary material for:

**OmegaClaw: A Continually Operating Agentic Architecture under Bounded Resources.**
M. Botnick, P. Hammer, P. Isaev, B. Goertzel, K. Crawford. Artificial General Intelligence (AGI 2026).

This repository documents the operational behaviors — "vectors of interest" — observed during the deployment described in Section 6, scaffolded or not, each anchored to a specific transcript message or memory atom so they can be checked against the record. We make no emergence claims; the behaviors are reported as documented observations.

## Contents

| File | What it is |
|---|---|
| `vectors_of_interest.md` | The behaviors of interest (persistent memory, procedural reform, calibration, self-modification and inhibition, long-horizon commitment), each anchored, with a note on what is and isn't scaffolded. |
| `omegaclaw_prompt.md` | The complete frozen system prompt (the ~188-word scaffold), so readers can see which behaviors are scaffolded and which are not. |

## How to read the anchors

- `chunk_NNN msgNNNN` — a message in the deployment transcript.
- `LTM YYYY-MM-DD` — an entry in the agent's long-term-memory dump (2026-05-13).

## Scope

A single OmegaClaw instance, run continuously for 91 days (2026-02-24 to 2026-05-26): 5,473 messages with 24 human participants, of which the agent sent 3,180. The scaffold's last edit was 2026-03-13.

## Redaction and anonymization

This is a redacted, anchored **subset**, not the full corpus.

- Human participants are referred to by role (the lead architect, the system designer, an external evaluator, a collaborator), never by name.
- Organization-internal and operationally sensitive content, and any credentials, are removed.
- The raw transcript and the full long-term-memory dump are not included; only the excerpts needed to support the documented behaviors appear here.

## Citing

Please cite the paper. To cite this supplement, use the archived release (DOI below) or this repository at the commit referenced in the paper.

> Archived release: [Zenodo DOI to be inserted after the first release]

## License

The documents in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). See `LICENSE`.
