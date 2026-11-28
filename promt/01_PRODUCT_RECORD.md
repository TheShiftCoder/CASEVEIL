# Product and Case Record — CASEVEIL / OBSCURA

## Identity and purpose
- Project/repository: CASEVEIL.
- Game: OBSCURA. Tagline: “Nothing is what it seems.”
- Genre: single-player, local-first, deterministic detective investigation mystery.
- Player role: independent detective investigating one contained homicide case.
- Product promise: investigate freely through scene examination, interviews, evidence comparisons, timeline and theory board; make a reasoned accusation and receive an evidence-based evaluation.
- V1 is a complete browser-playable prototype. No backend, account, database, paid service or AI API. Hardcoded logic and localStorage only.

## Core player loop
1. Enter the cinematic landing screen; start or resume the investigation.
2. Read case selection and briefing without learning the culprit.
3. Explore the study and other case locations; examine hotspots.
4. Interview five distinct suspects; ask about people, alibis and discovered evidence.
5. Collect and revisit evidence; compare supported evidence pairs.
6. Unlock timeline facts as evidence and testimony are found.
7. Build a board from discovered items, add/remove connections, and record theory notes.
8. Review notebook/case file and submit suspect, motive, method, evidence and explanation.
9. See scoring, reveal, true chronology, red herrings, replay/reset options.

## Case 001 — The Last Night at Blackwood
- Victim: Adrian Blackwood, wealthy art collector.
- Setting: Blackwood Estate during a storm that disrupts communications/security.
- Body found at 10:47 PM in the private study.
- Estimated death window: 9:30–10:20 PM.
- Five people were present. Intermediate difficulty.
- The player-visible briefing must not identify the culprit or disclose hidden truth.
- The original brief gives no definitive culprit, motive, murder method, suspect names or final clue solution. These must be authored as a single internally consistent case bible before the playable content is implemented. Never improvise conflicting facts in UI/dialogue.

## Case bible authoring requirements
Create exactly five suspects, each with public identity/role/relationship, personality, motive, public statement, alibi, private secret, private knowledge, truthful/false statements, interview triggers, and evidence reactions. Separate public facts from hidden truth. At least one suspect may lie for a non-murder reason.

Define a single canonical solution: culprit, motive, method, opportunity, sequence, death time, access path, concealment/cover story, and why the body is found at 10:47. Ensure every clue and statement is compatible with that solution.

Create at least 12 evidence items, with IDs, names, category, location, discovery prerequisites, player-facing initial and detailed descriptions, relevance, linked suspects/events, whether direct/circumstantial/red herring, and what new state they unlock. Undiscovered evidence must not appear in the player's archive.

Create chronological truth events and separately gated player-visible timeline events. Define contradictions as explicit pairs of claims/evidence, with prerequisites and resolution criteria. Define supported evidence comparisons and unsupported comparison responses. Define accusation scoring so culprit, motive, method, evidence strength and resolved contradictions each contribute transparently; wrong accusations cannot receive a correct-case ending.

## Screens and functions
Landing; case selection; briefing; investigation hub; crime scene; suspects/dedicated interrogation; evidence archive/details/filters; timeline/filters; detective board; notebook; case files; final accusation; results/reveal; settings; resume.
Every visible control must have a defined action, state effect, feedback, disabled/empty/error state where relevant, and keyboard/touch behavior.

## Visual system
- Background #0B0E13; secondary #10151D; panel #141B25; elevated #1A2230; border #293344.
- Primary text #E8EDF5; secondary #8995A7; muted #586477.
- Accent #C69A5D; hover #D9AD70; danger #B85B5B; success #799C84; investigation blue #7289A6.
- Inter/system sans for UI; restrained serif for cinematic titles.
- Dark, mature, cinematic, restrained. Thin borders, controlled spacing, subtle texture/motion. No neon, cartoon visuals, emoji UI or generic SaaS look.
- Desktop-first, fully usable on laptop/tablet/mobile. Mobile side panels become drawers; evidence board and scene hotspots remain operable by touch.

## Technical boundaries
React + Vite + JavaScript + CSS; React Router only if useful; Lucide React; localStorage. Modular UI, case data and engines. Deterministic logic; no API calls. Hidden solution must be separated from player-visible case data and never serialized into ordinary UI state or exposed in normal responses. Future AI services may replace engine interfaces without rewriting UI.

## Record decisions before build
- Confirm exact title usage: CASEVEIL is project; OBSCURA is game.
- Write and review the full Case 001 truth bible before coding dialogue/evidence.
- Define route/screen map, state schema, save version/migration and reset behavior.
- Define interaction feedback for every button, hotspot, filter, chip, form and board operation.
- Specify all empty, locked, discovered, selected, loading (if any), error, success and disabled states.
