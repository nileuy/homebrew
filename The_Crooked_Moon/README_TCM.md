# The Crooked Moon (Player) — Homebrew 5eTools

Este paquete contiene los archivos listos para subir al repo **TheGiddyLimit/homebrew** y/o cargar en 5eTools.

## Opciones de subida
- **Monolítico**: `monolithic/NiLe.Uy; The Crooked Moon (Player).homebrew.json` — contiene todas las categorías.
- **Dividido por tipo**: coloca cada JSON en su carpeta del repo (`subclass/`, `background/`, `feat/`, `spell/`).

## Cargar en 5eTools (local/web)
1. Abre *Utilities → Homebrew Manager*.
2. Usa **Load from File/URL** y selecciona el archivo monolítico.
3. Verifica visualmente las entradas.

## Metadatos
- Autor: **NiLe.Uy**
- Source ID/abbrev: **TCM**
- `_meta.sources` se incluye en cada archivo.

## Validación recomendada
```bash
npx -p 5etools-utils test-json-brew "ruta/al/archivo.json"
```
