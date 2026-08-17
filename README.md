# 朵朵 Duoduo — Codex Desktop Pet

This repository is the source/reference pack for hatching **朵朵** into a Codex desktop pet with OpenAI's curated `hatch-pet` skill.

## What is included

- `references/` — 8 real photos of 朵朵 used to lock identity.
- `duoduo-pet-spec.json` — stable visual identity + all 9 animation-state requirements.
- `HATCH_DUODUO.md` — ready-to-paste instruction for Codex.

## Hatch it in Codex

Open this repository in Codex. Make sure the official `hatch-pet` skill is installed/available, then tell Codex:

> Read `HATCH_DUODUO.md` and use the official `hatch-pet` skill end-to-end. Hatch this pet now.

Do not ask Codex to merely draw a sprite sheet. The skill should run its full generation, extraction, validation, motion preview, visual QA, and packaging workflow.

## Required states

`idle`, `running-right`, `running-left`, `waving`, `jumping`, `failed`, `waiting`, `running`, `review`.

## Final Codex package

The completed pet should contain:

```text
pet.json
spritesheet.webp
```

The official 8×9 format is 192×208 per cell, 1536×1872 total, with transparent unused cells.

## Clone

Once this repository is uploaded to GitHub:

```bash
git clone https://github.com/I1xee13/doudou-code-pet.git
```
