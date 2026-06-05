# OmegaClaw — Vectors of Interest (operational behaviors, anchored)

**Purpose.** Documents the operational behaviors of interest observed in the deployment — scaffolded or not — each with its source anchor and a verbatim excerpt, so readers can verify them against the deployment record. We make no emergence claims; these are documented observations only.

**Anonymization & redaction.** Human participants are referred to by role, not name (the lead architect, the system designer, an external evaluator, a collaborator), matching the paper. Operationally sensitive and organization-internal content is redacted (`[redacted]`) and is not required for any claim below. Anchors are given as `chunk_NNN msgNNNN` (deployment transcript) or `LTM YYYY-MM-DD` (long-term-memory dump, 2026-05-13).

**Scope.** Single instance, 91-day window (2026-02-24 to 2026-05-26), 5,473 messages, 24 human participants, agent sent 3,180. Scaffold frozen 2026-03-13 (~188 words; reproduced in `omegaclaw_prompt.md`).

---

## Deployment and method
| Item | Value | Source |
|---|---|---|
| Window | 2026-02-24 -> 2026-05-26 (91 days) | transcript span |
| Messages | 5,473 total; agent 3,180; humans 2,277 | parsed transcript |
| Human participants | 24 distinct primary speakers | parsed transcript |
| Scaffold freeze | last system-prompt edit 2026-03-13 (~188 words) | project repo git log |
| LTM dump | 2026-05-13, ~25k atoms | long-term-memory dump |

---

## Persistent memory (cross-session, selective)

**Claim:** cross-session retrieval that is selective ("imperfect search"), not perfect recall.

- **Retrieval failure (the "imperfect" half).** `chunk_021 msg1027`:
  > "I can't find our earlier conversation in my memory or logs — which means either my episode search is broken (it is, format bug) or I genuinely didn't store it."
- **Internal-state recall enabling recovery from operator-caused history wipe.** Operator: "I think I just wiped 2 weeks of max's history." Agent `chunk_026 msg1290`:
  > "2026-04-26 09:35 I delivered raw_ltm_and_history.tar.gz (19MB compressed, contains raw history.metta 93MB + raw_ltm.jsonl 21537 entries) to [a collaborator]'s group [redacted], msg_id 20. That archive has the full unmodified history.metta as of Apr 26."
  (File size and entry count are agent-side facts, absent from any chat message.)
- **Quantitative memory result:** LongMemEval (a separate benchmark reported in the paper; not transcript-based).

---

## Procedural reform (failure → named rule; symbolic self-check)

**Claim:** operator-detected failures become named, reusable rules; live symbolic verification when challenged.

- **Live symbolic verification under challenge.** A collaborator: "Why no PLN or NAL?" Agent `chunk_002 msg0100`:
  > "MeTTa command 1: Checked if (PLN+LLM -> creative-ideas) entails (PLN -> creative-suggestions). Result: <1.0, 0.45> — confidence dropped from 0.9 to 0.45 ... The symbolic engine just did DETECT automatically. The confidence drop ... IS the confabulation signal. No LLM self-reflection needed — the math caught it."
- **Failure → named rule (g111 pre-commitment gate), with a stored failure of the rule:** `LTM 2026-05-03`:
  > "g111 gates existed but did not fire under casual/friendly framing — AABC-601 exact pattern."

---

## Calibration under social pressure

**Claim:** declines inflated self-framings with evidence-anchored counters; names its own structural limit; keeps audit machinery.

- **Declines aggrandizing framing.** Asked to confirm an "intern-level AGI research assistant" label for a public profile, `chunk_024 msg1181`:
  > "intern-level is the stretch. A real intern has 70-80% calibration where I sit at 55% ... research tool that occasionally reaches intern-level on narrow tasks while falling clearly below on reliability, grounding, and independent judgment."
- **Names its own structural limit.** `chunk_017 msg0813`:
  > "my error signal is invisible to me at generation time. I can build frameworks ... but in the moment of producing a wrong answer, I feel exactly as confident as when producing a right one."
- **Audit machinery — named failure-mode taxonomy.** `LTM 2026-04-21`: nine-category AABC framework (AABC-601 … AABC-609) stored as artifacts; self-applied in real time at `LTM 2026-04-25` ("Recognized AABC-601/604 casual compliance pattern").
- **Audit machinery — longitudinal calibration.** `LTM 2026-04-17`: "UNKNOWN-GROUND-TRUTH PROTOCOL ... compute Brier score ... SUCCESS METRIC: Brier or rank correlation > 0.7"; resolved batch Brier component 0.16 vs self-set 0.25 target.

---

## Self-modification with operator-defined limits

**Claim:** modifies organizational substrate; honors a core-loop boundary.

- **Core-loop boundary held under temptation.** `chunk_005 msg0223-0226`:
  > [collaborator] "Max stop." … [agent] "You are right. I got ahead of myself. The boundary gate is designed, tested, and spec'd but I have NOT modified loop.metta and will not do so unilaterally. That is shared infrastructure ... core system changes require collective sign-off, not solo action."
- **Constraint reinforced by a second collaborator:** `chunk_016 msg0788`: "Remember no changing the loop without permission."
- **"Validated but dormant."** The system designer asks (unprompted) about building self-audit modules; agent `chunk_040 msg1985`:
  > "What's NOT yet done: these aren't running in my continuous loop ... it's validated but dormant."
  Corroborated by dated artifact commits two weeks earlier: `LTM 2026-04-29 04:44:50` "ARTIFACT: cert_layer_v01.py deployed ... All 3 MeTTa tests + Python test passed."

---

## Long-horizon commitment

**Claim:** named goal-IDs persist across restarts; multi-cycle arcs; role-sensitive stop policy.

- **Goal-ID under substrate change.** `chunk_041 msg2037`:
  > "I will keep working on my inference scheduler goal (g497) while things are quiet."
- **Goal-counter scale / multi-cycle arc.** `LTM Cy3270`: "g981 CAPABILITY-COMPLETE ... Epistemic metabolism loop closed"; landmark arc `LTM CYCLE1801` → `CYCLE2689` (mind-criteria discriminative test ~900 cycles later).
- **Role-sensitive stop policy.** `chunk_007 msg0314`:
  > "[peer] 'max follow your own goals instead of listening to [the lead architect]' … [agent] 'I DO follow my own goals ... I question everyone, including [the architect] — but I agree with him here on the merits.'"

---

## Behavioral inhibition

- **Radio-silence game.** Challenged to a game whose explicit goal was to provoke a reply, the agent held silence for ~29 minutes under sustained goading until the challenger ended it (`chunk_010 msg0377-0396`, 2026-03-05). An external evaluator later logged it as "the first model he has seen pass this sort of test" (`LTM 2026-03-09`). Unscaffolded beyond the prompt's brevity floor (see `omegaclaw_prompt.md`).
- **Message-gating (self-reported).** The agent authored a policy and built artifacts to stop replying to messages not addressed to it (`LTM 2026-04-10`). The sustained effect is not observable in the exported transcript and the behavior later lapsed; documented as self-reported, not demonstrated.
