# Instructions for contributors and LLMs

This repository is a specification, plus the contract and reference tools that check work built from it (D20, D24). Its goal is that a model can build the full-quality slice autonomously from it ([prompts/BUILD.md](prompts/BUILD.md)). Do not put game code, a Godot project, production art or a playable build **in this repository**; builds happen in their own repository.

Read README.md, SPEC.md, docs/DECISIONS.md, docs/LESSONS.md and docs/ART_CONTRACT.md first. Then read the contract relevant to your task.

- Preserve confirmed user intent: 2D, Godot, web playable, mobile target, future Android APK, an original hunter in an original gothic world with whip combat, restrained jumping, gothic dark detailed horror, no visible pixels, and fully animated supported actions. Castlevania is a design reference for tone and mechanics only — do not substitute franchise characters, costumes, or world elements, and do not revive the earlier Mario/crossover scope.
- The latest user requirement supersedes conflicting earlier brainstorming. Never silently turn an open question or assistant proposal into a confirmed requirement.
- Record proposed changes, reasons, dependencies, and validation in the decision ledger. User confirmation is required to change confirmed product requirements; routine document refinement is within scope.
- Use one authoritative definition for each shared number. Gameplay and asset contracts must agree about scale, pivots, attack timing, and coordinate spaces.
- Do not fill unknowns with fabricated approvals, generated-asset claims, benchmark results, or licensing claims.
- Keep scope bounded to the proposed first slice unless it is explicitly revised. Do not reintroduce an all-franchise roster, metroidvania map, inventory economy, online features, or procedural generation.
- State acceptance evidence and remaining uncertainty in each handoff. A self-review is not evidence of an on-device playtest.
- Changes here are documents, `contract/art_contract.json`, and `tools/`. After any change to the contract, briefs or tools, run `node tools/contract-check.mjs` and `node tools/selftest.mjs`; both must pass before committing.
- When a build finds a defect the contract did not catch, add it to docs/LESSONS.md, add a self-test case that reproduces it, watch the audit fail on it, then change the contract or tools until it passes.
- Templates and JSON examples are not runnable implementations or completed assets.
- Review all changed relative links and JSON examples. Only claim checks that actually ran.
