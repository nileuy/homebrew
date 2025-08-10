# The Crooked Moon — 5eTools Data (Player)
Source ID: `TCM`

This package contains 5eTools JSON files extracted and formatted from the **The Crooked Moon — Player PDF (2024)**.

## Contents
- `data/tcm/sources.json` — Source metadata (TCM)
- `data/tcm/races.json` — Races (if present)
- `data/tcm/subclasses.json` — Subclasses + Class Features (autolinked to TCM spells)
- `data/tcm/backgrounds.json` — Backgrounds
- `data/tcm/feats.json` — Origin feats (fine-formatted with items)
- `data/tcm/spells.json` — Spells (refined ranges & “At Higher Levels” sectioned)

## Notes
- Cross-references to TCM spells are auto-linked using `{@spell Name|TCM}` in feats, subclasses, and backgrounds.
- Ranges like “Self (30-foot cone)” are converted to native 5eTools AoE shapes.
