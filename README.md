# Gothic Whip — specification

A specification repository for a **2D gothic horror platformer starring an original hunter in an original gothic world, with whip-led combat and restrained jumping**, made in Godot for mobile browser play, with Android APK support planned later. Castlevania is the design reference for tone and mechanics only.

**Goal:** concrete enough that a model can build the full-quality slice from it without a human reviewing the art (D20, D21). **Status:** specification complete on paper (packages P0–P6) with a measurable art contract, reference tools that check it, and lessons from one complete implementation ([askjackb/gothic-whip-game](https://github.com/askjackb/gothic-whip-game), see [docs/LESSONS.md](docs/LESSONS.md)). No engine project, art or build lives here. "Gothic Whip" is a working label, not an approved title.

**To build the game:** use [prompts/BUILD.md](prompts/BUILD.md). **To check the contract:** `node tools/contract-check.mjs && node tools/selftest.mjs` (Node 20+, no install).

## Start here

1. [SPEC.md](SPEC.md): product boundary, gameplay contract, proposed first slice, acceptance gates.
2. [Decision ledger](docs/DECISIONS.md): confirmed intent versus proposed defaults and open decisions.
3. [Art direction](docs/ART_DIRECTION.md): visual grammar and style calibration.
4. [Asset specification](docs/ASSET_SPEC.md): dimensions, animation, export, metadata, and rejection rules.
5. [Asset generation instructions](prompts/ASSET_GENERATION.md): reusable briefing and review prompts.
6. [Next-LLM prompt](prompts/NEXT_LLM.md): the exact task to begin with.
7. [Full animation contract](docs/ANIMATION_SPEC.md): required states, transitions, and completeness gates.
8. [Work packages](docs/WORK_PACKAGES.md): bounded follow-on specification tasks.
9. [Technical constraints](docs/TECHNICAL_CONSTRAINTS.md), [technical spec](docs/TECHNICAL_SPEC.md) and [validation plan](docs/VALIDATION.md).
10. [Gameplay rules](docs/GAMEPLAY_RULES.md), [stage design](docs/STAGE_DESIGN.md), [art bible](docs/ART_BIBLE.md), [asset briefs](docs/ASSET_BRIEFS.md), [texture budget](docs/TEXTURE_BUDGET.md).
11. **[Art contract](docs/ART_CONTRACT.md)**: measurable acceptance for every frame, the independent reviewer gate, and why each rule exists. Machine-readable form: [contract/art_contract.json](contract/art_contract.json). Tools: [tools/](tools/README.md). Reviewer prompt: [prompts/ART_REVIEW.md](prompts/ART_REVIEW.md).
12. [Lessons from the first implementation](docs/LESSONS.md).

Use [the asset brief](templates/ASSET_BRIEF.md), [manifest example](templates/asset-manifest.example.json), and [decision template](templates/DECISION.md) when filling gaps.

## The controlling idea

The horror and combat come first. Platforming creates spacing, elevation, and tension; it does not demand Mario's acrobatic mobility. The final direction is primarily Castlevania. Earlier Mario/crossover brainstorming is superseded as the core direction. No visible pixel art is allowed, and every supported character action requires a complete animation, including crouching, jumps, knockback, recovery, and death.

This repository distinguishes **CONFIRMED**, **PROPOSED**, **OPEN**, and **DEFERRED** decisions. Proposed defaults make the framework concrete; they are not user approvals. Other LLMs should refine the documents and expose contradictions before producing a game or a large asset batch.

Character/franchise references describe creative intent. No third-party game files, sprites, music, logos, or reference-image binaries are included, and this repository does not grant rights to those properties. Future assets must record their provenance separately.
