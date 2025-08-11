# The Crooked Moon — Player Options (5eTools Homebrew)

This repository contains **player options** from *The Crooked Moon* formatted for **5eTools**/**Plutonium**.

> **Includes**
> - **Spells**: 26
> - **Species** (races): 13
> - **Subclasses**: 3 (features: 14)
> - **Feats**: 14
> - **Backgrounds**: 13

---

## Quick Start (Import)

1) Download this repository (or just the JSON files under `/tcm_homebrew`).  
2) In **5eTools** / **Plutonium**, open **Manage Homebrew → Load from File**.  
3) Select the collection file:
   - `TCM; The Crooked Moon — Player Options (collection).json`  
   This will import all component JSONs in one go:
   - `tcm-spells.brew.json`
   - `tcm-species.brew.json`
   - `tcm-subclasses.brew.json`
   - `tcm-feats.brew.json`
   - `tcm-backgrounds.brew.json`

> You can also import files individually if preferred.

---

## Files

```
tcm_homebrew/
├─ TCM; The Crooked Moon — Player Options (collection).json
├─ tcm-spells.brew.json
├─ tcm-species.brew.json
├─ tcm-subclasses.brew.json
├─ tcm-feats.brew.json
├─ tcm-backgrounds.brew.json
└─ tcm-collection.json        # helper manifest (non-standard, informational)
```

- **collection.json** (`TCM; ...`): `toImport` list pointing to the five brew JSONs.
- **tcm-*.brew.json**: Each file conforms to the **5eTools brew schema** (`spell`, `race`, `subclass`+`subclassFeature`, `feat`, `background`).
- **tcm-collection.json**: Helper map used during generation; safe to ignore.

---

## Validation

- JSONs follow the **brew schema** for 5eTools.  
- A local preflight was run to check required keys and basic shapes.  
- If you use the official validator, run something like:

```bash
# Example (adjust to your environment)
npx --yes @thegiddylimit/5etools-utils test-json-brew tcm-spells.brew.json
npx --yes @thegiddylimit/5etools-utils test-json-brew tcm-species.brew.json
npx --yes @thegiddylimit/5etools-utils test-json-brew tcm-subclasses.brew.json
npx --yes @thegiddylimit/5etools-utils test-json-brew tcm-feats.brew.json
npx --yes @thegiddylimit/5etools-utils test-json-brew tcm-backgrounds.brew.json
```

---

## Contributing / Editing

- Keep entries **English**, verbatim to the source rules text where applicable.  
- Maintain consistent `source: "TCM"` and `page: 0`.  
- For spells:
  - Normalize `range.area` for **Self (X‑foot cone/line/sphere/cube/cylinder)**.
  - Use `entriesHigherLevel: [{"name":"At Higher Levels","entries":[...]}]`.
  - `classes.fromClassList` with `{ "name": "Bard", "source": "PHB" }` etc. (Artificer → `TCE`).

---

## Credits & Legal

- **Source**: *The Crooked Moon — Player Options*.  
- This repo is a **fan-made homebrew adaptation** for use with 5eTools/Plutonium.  
- All trademarks and copyrights remain with their respective owners.

---

## Changelog

- **2025-08-11** — Initial public version: spells/species/subclasses/feats/backgrounds + collection.
