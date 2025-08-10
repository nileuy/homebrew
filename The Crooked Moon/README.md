# The Crooked Moon — 5eTools Homebrew (TCM)

> Fuente: *The Crooked Moon — Player Options (2024)*  
> `json` ID: **TCM** · `edition`: **one** (2024) · Versión: **1.0.3**

## Contenido del paquete
```
content/
  collection/
    TCM.homebrew.json          # Monolítico (todo en uno) — recomendado
  spell/
    TCM-spells-brew.json
  subclass/
    TCM-subclasses-brew.json
  feat/
    TCM-feats-brew.json
  background/
    TCM-backgrounds-brew.json
  race/
    TCM-species-brew.json
validation-report.json         # Informe preflight (no reemplaza al validador oficial)
```

## Cómo validar localmente
Requisitos: Node.js 18+

```bash
# Validar el monolítico
npx -y 5etools-utils@latest test-json-brew ./content/collection/TCM.homebrew.json

# (Opcional) Validar por tipo
npx -y 5etools-utils@latest test-json-brew ./content/spell/TCM-spells-brew.json
npx -y 5etools-utils@latest test-json-brew ./content/subclass/TCM-subclasses-brew.json
npx -y 5etools-utils@latest test-json-brew ./content/feat/TCM-feats-brew.json
npx -y 5etools-utils@latest test-json-brew ./content/background/TCM-backgrounds-brew.json
npx -y 5etools-utils@latest test-json-brew ./content/race/TCM-species-brew.json
```

> Tip: el validador reporta **un error por vez**. Corregí el primero, re-ejecutá, y repetí hasta `OK`.

## Carga en 5eTools
1. Abrí **Utilities → Homebrew Manager** en 5eTools.  
2. Usa **Load from File** y seleccioná `content/collection/TCM.homebrew.json`.  
   —o— subí el archivo a GitHub y usá el **RAW URL** en **Load from URL**.
3. Filtrá por **Source: TCM** para revisar todo.

## Notas de conversión
- **subclassSpells**: nombres de hechizos **sin asteriscos** y alineados con los del propio brew cuando aplica.
- **Harvest Domain**: el PDF separa por aspectos (Sowing/Growing/Reaping). En 5eTools cargamos la **unión** por nivel y el texto del feature indica la elección.
- **Autolink** aplicado: `{@spell ...}`, `{@condition ...}`, `{@skill ...}` en textos.
- **Especies**: `Small or Medium` → `size: ["M","S"]` cuando corresponde.

## Sugerencia de PR (nombre de archivo)
Si subís por tipo al repositorio homebrew oficial, usá el patrón:  
`Autor; The Crooked Moon — Player Options (2024).json`  
o mantené el monolítico como `TCM.homebrew.json` dentro de `collection/`.

---

Hecho con ❤️ para 5eTools. Si encontrás algún error en el validador, compartime el mensaje y lo arreglo.
