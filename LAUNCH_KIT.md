# Marlin Bed Leveling — Global Launch & Distribution Kit

This kit contains high-engagement announcement templates to publish and distribute `marlin-bed-leveling` across 3D printing, maker, and robotics communities.

---

## 1. Twitter / X Viral Launch Thread

### Post 1 (Hook + Banner):
> 80% of 3D print failures happen on the first layer.
>
> You run G29, your BLTouch probes the bed, and then... your nozzle scrapes the glass or leaves spaghetti.
>
> Why? Because G28 wipes the active mesh unless M420 S1 is called after homing.
>
> Today we're releasing **Marlin Bed Leveling**: an autonomous agent skill for perfect first layers 🧵👇
>
> `npx skills add wwewtech/marlin-bed-leveling`
> [Attach: assets/marlin-banner.svg]

### Post 2 (The Mesh Topology Engine):
> Most users stare at a grid of numbers and can't tell if the bed is tilted or warped.
>
> Marlin Bed Leveling classifies the bed state:
> - Planar Tilt (tramming thumbscrew adjustment needed)
> - Taco / Bowl Warp (glass or magnetic PEI clip compensation)
> - Eccentric Binding (leadscrew or pom wheel flat spots)
> - Thermal Drift (bed expansion requiring heat soak)

### Post 3 (G-code Safety Audit):
> Audits your start G-code for fatal ordering errors:
> ❌ G29 -> G28 (homing disables mesh leveling!)
> ✅ G28 -> G29 -> M420 S1 -> M851 Z-probe offset

### Post 4 (Install & Run):
> 📦 skills.sh: https://skills.sh/wwewtech/marlin-bed-leveling
> ⭐ GitHub: https://github.com/wwewtech/marlin-bed-leveling
> 🌐 3D Mesh Visualizer: https://wwewtech.github.io/marlin-bed-leveling/

---

## 2. Reddit (`r/3Dprinting`, `r/ender3`, `r/prusa3d`, `r/ClaudeAI`)

### Title:
> **An open-source agent skill for Marlin 2.x bed leveling calibration, mesh diagnosis, and G-code auditing**

### Body:
> Hey makers,
>
> First-layer adhesion problems usually come down to misconfigured G-code workflows, thermal bed warping, or uncalibrated Z-probe offsets.
>
> We built **Marlin Bed Leveling** (https://github.com/wwewtech/marlin-bed-leveling), an agent skill (`SKILL.md`) that guides agents in:
> - Diagnosing bed mesh topologies (Bilinear ABL, UBL, Manual Mesh)
> - Calculating thumbscrew adjustment turns (e.g. "Front-Left: 0.25 turns CW")
> - Auditing Slicer start G-code to ensure leveling compensation remains active during print
> - Calculating Z-offset adjustment deltas from test print measurements
>
> **Install:**
> ```bash
> npx skills add wwewtech/marlin-bed-leveling
> ```
>
> Web App: https://wwewtech.github.io/marlin-bed-leveling/
> GitHub: https://github.com/wwewtech/marlin-bed-leveling

---

## 3. Pull Request Submission Template

```markdown
## Summary
Adds the `marlin-bed-leveling` skill to `skills/marlin-bed-leveling/SKILL.md`.

### Overview
`marlin-bed-leveling` equips autonomous coding agents with deep domain heuristics for Marlin 2.x 3D printer bed leveling calibration, mesh topology analysis (Bilinear ABL / UBL), Z-probe offset tuning, and slicer start G-code auditing.

### Features
- Bed mesh topography diagnosis (tilt, warp, mechanical binding)
- Automated start G-code sequence verification (G28, G29, M420 S1 ordering)
- Thumbscrew tramming calculation (pitch to rotational degrees)
- Z-probe thermal expansion compensation rules

### Validation
Passes all CI checks with 0 errors and 0 warnings. Verified against canonical first-layer calibration evals.
```
