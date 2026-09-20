---
name: marlin-bed-leveling
description: Calibrate Marlin firmware bed leveling (UBL, Bilinear, Manual Mesh) with an agent: G29 phase workflow, G26 validation prints, M421 mesh edits, EEPROM slots, probe offsets, and LCD-less flows. Use when the user runs Marlin (not Klipper) and fights first-layer adhesion, warped beds, or probe setup. Never move the nozzle into the bed blindly.
---

# Marlin Bed Leveling Tuner

First-layer problems on Marlin are almost always mesh problems. This skill drives the full calibration loop: configure → probe → validate → fine-tune → save.

## Scope

- Marlin 2.x with `AUTO_BED_LEVELING_UBL`, `AUTO_BED_LEVELING_BILINEAR`, or `MESH_BED_LEVELING`.
- Assumes a working printer that already homes (`G28`) and extrudes. Not a first-build guide.
- Operates via terminal/OctoPrint G-code console. If the printer runs from SD card with no host link, switch to guided mode: give the user exact commands to type, one step at a time.

## When NOT to use

- Klipper printers — different system (use a Klipper skill instead).
- Delta kinematics quirks beyond stock UBL probing — say so explicitly.
- Hardware faults (dead probe, loose couplers, wobbling frame) — leveling cannot fix mechanics; diagnose first.

## Method

1. **Identify setup.** Ask or detect: leveling type enabled in firmware, probe type (BLTouch/CRTouch/inductive/none), LCD present or not, EEPROM enabled (`M500` works?).
2. **Baseline first.** Never start UBL on a printer that cannot print a small centered object with leveling off. Verify `NOZZLE_TO_PROBE_OFFSET` — a wrong offset bakes dimensional error into every mesh.
3. **Build the mesh (UBL).**
   - `G29 P0` zero, `G29 P1` auto-probe, `G29 P3` smart-fill unreachable points (repeat as needed), `G29 T` inspect map.
   - No LCD: skip `P2`, use `P3` fill + `M421` edits instead.
   - No probe: `G29 P0`, manual `P2` paper probing, then `P3` fill.
   - Set fade: `G29 F10.0`. Save: `G29 S0`, `M500`. Activate: `G29 A`.
4. **Validate with plastic.** Run `G26 C P T3.0` mesh validation pattern (or any bed-level test print). Read the result: gaps = too high, ridges/rough = too low, per region.
5. **Fine-tune.** `G29 P4 T` (move to bad areas, adjust) or `M421 I<J> J<I> Z<offset>` / `M421 Q` offsets without LCD. Re-run validation. Save with `G29 S0` + `M500`.
6. **Startup G-code.** Ensure prints load the mesh: `G29 L0` then `G29 J` (3-point tilt) or `M420 S1`. Without this the mesh silently does nothing.

## Safety rules

- Never command Z motion toward the bed without a known-good offset; manual `P2`/`P4` moves are crash-capable — go slow, abort on resistance.
- `M502` (factory reset) only with explicit approval — it wipes the mesh and all tuning.
- EEPROM slot discipline: note which slot holds the good mesh; do not overwrite slot 0 blindly.

## Key references (verify against installed Marlin version — G-code varies)

- `G29` phases P0–P6, S/L/A/D/T/F/J; `G26` validation; `M421` mesh edit; `M420 S1/V`; `M500/M501/M502`; `M114` position check.
- Sources: `marlinfw.org/docs/gcode/G029-ubl.html`, `marlinfw.org/docs/features/unified_bed_leveling.html`.
