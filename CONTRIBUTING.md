# Contributing to Aphidex-Data / Contribuir a Aphidex-Data

## Quick rules / Reglas rápidas
**EN:**
- Do not change existing `id` values.
- `tier` is an integer: 1–5 (Boss = 5).
- `danger` must be one of: `baja`, `media`, `intermedia`, `alta`, `muy_alta`, `extrema`, `imposible`.
- `weaknesses` and `resistances` are arrays of IDs (see below).
- Keep JSON valid. Use a JSON formatter before submitting.

**ES:**
- No cambies `id` existentes.
- `tier` es entero: 1–5 (Boss = 5).
- `danger` solo puede ser: `baja`, `media`, `intermedia`, `alta`, `muy_alta`, `extrema`, `imposible`.
- `weaknesses` y `resistances` son arreglos de IDs (ver abajo).
- Mantén el JSON válido. Formatea antes de enviar.

## Allowed IDs / IDs permitidos
**Damage types / Daños:**
- `slashing`, `chopping`, `busting`, `stabbing`, `explosive`, `generic`, `dust`

**Elementals / Elementales:**
- `fresh`, `spicy`, `salty`, `sour`

**Status / Estados:**
- `poison`, `venom`, `infection`

**Weak points / Puntos débiles (v2):**
- `back`, `eyes`, `gut`, `legs`, `rump`

**Susceptible damage (v2):**
- `any`, `stabbing_arrows_only`, `stabbing`, `chopping_and_slashing`, or any damage ID above.

**Weak point + susceptible damage rules / Reglas de punto débil + daño susceptible:**
- `back`: `any`
- `eyes`: `stabbing_arrows_only`
- `gut`: `stabbing`
- `legs`: `chopping_and_slashing`
- `rump`: `any`

## File locations / Ubicación de archivos
- Grounded 1 data: `data/grounded1/enemies_g1.json`

## PR checklist / Checklist del PR
- [ ] JSON is valid (no trailing commas).
- [ ] No `null` on required fields (`id`, `name`, `game`, `danger`, `cardNormal`, `cardGold`, `photo`).
- [ ] `tier` is integer 1–5.
- [ ] `danger` uses allowed values.
- [ ] Paths follow the app conventions (do not invent new folders).
- [ ] Briefly describe the change in the PR.
