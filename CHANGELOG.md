# Changelog

All notable changes to the `marlin-bed-leveling` skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2026-09-22

### Initial Release — Marlin 2.x Bed Leveling & Mesh Calibration

#### Added
- **Master Skill (`SKILL.md`):** Complete calibration standard for UBL, Bilinear ABL, and MBL.
- **The Post-Homing Rule:** Slicer start sequence enforcing `M420 S1 Z10.0` strictly after `G28`.
- **Negative Z-Probe Offset Math:** Polarity rules preventing nozzle PEI crashes.
- **Thermal Stabilization Invariant:** 5-minute pre-heat soak requirements for aluminum beds.
- **Interactive Topography Simulator (`docs/index.html`):** 5x5 interactive mesh visualizer and feeler gauge tester.
- **CI Validation:** Automated YAML frontmatter and SHA256 file symmetry verification.
