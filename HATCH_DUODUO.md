# Hatch Duoduo — Codex instruction

Use the installed official `hatch-pet` skill end-to-end to hatch a Codex-compatible desktop pet named **Duoduo / 朵朵**.

## Grounding references
Use ALL images in `./references/` as identity references. They are photos of the same dog.

## Visual direction
Create a **realistic but gently cartoonized** version of Duoduo:
- preserve her real small-dog body proportions rather than turning her into an oversized-head chibi;
- preserve fluffy white coat texture, big round dark eyes, small black nose, cream-tinted longer muzzle/moustache fur, drop ears, short legs;
- keep the same face, coat, proportions, palette and silhouette across every animation state;
- make the sprite clean and readable at Codex pet size, but still recognizably the real Duoduo;
- transparent final background; no scene backgrounds, labels, UI, text, logos, glow, shadow blobs, motion trails, dust, or speed lines.

Read `duoduo-pet-spec.json` and treat it as authoritative for identity and animation semantics.

## Required states
Use the official Codex 9-state order:
1. idle
2. running-right
3. running-left
4. waving
5. jumping
6. failed
7. waiting
8. running
9. review

Special requirements:
- `waiting`: create an attentive waiting loop. Include the special gesture naturally adapted to dog anatomy: right front paw moves from beside the right eye down toward the neck/chest twice; left front paw stays still.
- `running`: this is the Codex working state, not directional running. Have Duoduo happily eat/carry a small bread or toast prop while mostly staying in place.
- `review`: focused reading/reviewing beside a small neutral laptop or document; round glasses are allowed.
- The blue-trim transparent raincoat from the references is an optional prop only when it improves a state; do not force it into every row.

## QA and packaging
Follow the hatch-pet skill exactly for:
- row generation,
- frame extraction,
- transparency,
- atlas geometry,
- motion preview QA,
- identity consistency QA,
- final validation,
- packaging.

Do not fake missing rows by locally duplicating, transforming, or code-drawing other states.

Final output must be the Codex pet package containing:
- `pet.json`
- `spritesheet.webp`

Install/package it under the normal Codex pet path for a pet id of `duoduo` (or the closest valid normalized id chosen by the skill).

When finished, tell me the exact output folder path and whether all validation and visual QA checks passed.
