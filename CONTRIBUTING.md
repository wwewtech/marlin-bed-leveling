# Contributing to Marlin Bed Leveling

We welcome contributions from 3D printing enthusiasts, firmware hackers, and maker community engineers.

---

## Ways to Contribute

1. **Slicer Profiles:** Add start G-code macros for additional slicers (e.g., Kiri:Moto, Simplify3D, SuperSlicer).
2. **Kinematic Configurations:** Provide tuning presets for coreXY or dual-Z independent leveling (`G34 Z_STEPPERS_AUTO_ALIGN`).
3. **Evals (`evals/evals.json`):** Contribute real-world first-layer adhesion issues and sensor repeatability bugs.

---

## Submission Guidelines

- Ensure byte-for-byte SHA256 symmetry between `./SKILL.md` and `./skills/marlin-bed-leveling/SKILL.md`.
- Maintain single-file self-containment in `SKILL.md`.
- Validate before opening a PR:
  ```bash
  python -c "import hashlib; assert hashlib.sha256(open('SKILL.md','rb').read()).hexdigest() == hashlib.sha256(open('skills/marlin-bed-leveling/SKILL.md','rb').read()).hexdigest(), 'Hash mismatch!'"
  ```
