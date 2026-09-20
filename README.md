# marlin-bed-leveling

Calibrate Marlin firmware bed leveling (UBL, Bilinear, Manual Mesh) with an agent: G29 phase workflow, G26 validation prints, M421 mesh edits, EEPROM slots, probe offsets, and LCD-less flows.

## Why this skill?
First-layer problems on Marlin are almost always mesh problems. This skill drives the full calibration loop: configure → probe → validate → fine-tune → save. It guides AI agents to correctly assist with Marlin bed leveling using best practices.

## Quick Installation

### 1. Via `skills.sh` / Vercel Skills CLI
```bash
npx skills add wwewtech/marlin-bed-leveling
```

### 2. Via Claude Code
```bash
claude skills add https://github.com/wwewtech/marlin-bed-leveling
```

### 3. For Google Antigravity
Clone or copy `SKILL.md` directly into your Antigravity skills directory:
```bash
# Windows
mkdir -p "$HOME\.gemini\config\skills\marlin-bed-leveling"
curl -sL https://raw.githubusercontent.com/wwewtech/marlin-bed-leveling/main/SKILL.md -o "$HOME\.gemini\config\skills\marlin-bed-leveling\SKILL.md"

# macOS / Linux
mkdir -p ~/.gemini/config/skills/marlin-bed-leveling
curl -sL https://raw.githubusercontent.com/wwewtech/marlin-bed-leveling/main/SKILL.md -o ~/.gemini/config/skills/marlin-bed-leveling/SKILL.md
```

### 4. For Cursor & Windsurf
Add `SKILL.md` to your workspace prompt context:
```bash
mkdir -p .cursor/skills/marlin-bed-leveling
curl -sL https://raw.githubusercontent.com/wwewtech/marlin-bed-leveling/main/SKILL.md -o .cursor/skills/marlin-bed-leveling/SKILL.md
```

## Links
- [Live Showcase](https://wwewtech.github.io/marlin-bed-leveling/)
- [skills.sh](https://skills.sh/wwewtech/marlin-bed-leveling)
- [SKILL.md](./SKILL.md)

## Core Concepts
- Uses G29 (UBL/Bilinear) or MESH_BED_LEVELING
- Configures probe offsets and fade heights
- Fine-tunes meshes with M421 and G26 validation
- Manages EEPROM carefully with M500/M501/M502

## License
MIT © 2026 wwewtech (Pavel Lebedev)
