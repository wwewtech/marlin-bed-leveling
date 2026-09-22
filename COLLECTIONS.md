# Complete Distribution & Collections Directory

This registry catalogs **`marlin-bed-leveling`** across every AI agent directory, Cursor rule repository, Claude Code showcase, awesome-list, and community distribution channel.

---

## 1. Official Registries & Package Hubs

| Platform | Type | Link / Command | Submission Method | Status |
| :--- | :--- | :--- | :--- | :--- |
| **skills.sh** (Vercel) | Universal CLI Registry | [skills.sh/wwewtech/marlin-bed-leveling](https://skills.sh/wwewtech/marlin-bed-leveling) | Git Tag / Auto-Indexed | Indexed & Verified |
| **Anthropic Official Skills** | Show & Tell Showcase | [Anthropic Skills Forum](https://github.com/anthropics/skills/discussions) | Official Community Forum | Ready to Publish |
| **Cursor Directory** | Cursor Rules Hub | [cursor.directory](https://cursor.directory/) | Form / GitHub PR | Ready to Submit |
| **Awesome Claude** | Claude Code Hub | [awesomeclaude.ai](https://awesomeclaude.ai/) | "Submit Resource" / PR | Ready to Submit |
| **Cline Rules Hub** | Roo Code / Cline Directory | [clinerules.org](https://clinerules.org/) | GitHub PR | Ready to Submit |
| **Smithery.ai** | Agent Capabilities Registry | [smithery.ai](https://smithery.ai/) | Indexed via `smithery.json` | Manifest Configured |
| **Glama.ai** | Agent Tools & MCP Hub | [glama.ai/mcp](https://glama.ai/mcp) | Web Submission | Ready to Submit |

---

## 2. GitHub Awesome-Lists Submissions & PR Tracker (20 Curated Targets)

| Repository | Focus / Category | Status |
| :--- | :--- | :--- |
| **sickn33/agentic-awesome-skills** (46,500+ ⭐) | AAS Core / `skills/marlin-bed-leveling/SKILL.md` | [PR #1562](https://github.com/sickn33/agentic-awesome-skills/pull/1562) |
| **ComposioHQ/awesome-claude-skills** (75,000+ ⭐) | `Hardware, 3D Printing & Manufacturing` | [PR #1962](https://github.com/ComposioHQ/awesome-claude-skills/pull/1962) |
| **heilcheng/awesome-agent-skills** (6,200+ ⭐) | `Hardware & Additive Manufacturing` | [PR #517](https://github.com/heilcheng/awesome-agent-skills/pull/517) |
| **VoltAgent/awesome-agent-skills** (34,500+ ⭐) | `Community Skills -> Hardware & 3D Printing` | [PR #1092](https://github.com/VoltAgent/awesome-agent-skills/pull/1092) |
| **PatrickJS/awesome-cursorrules** (10,000+ ⭐) | `3D Printing / G-code / Embedded` (`rules/marlin-bed-leveling.mdc`) | [PR #391](https://github.com/PatrickJS/awesome-cursorrules/pull/391) |
| **BehiSecc/awesome-claude-skills** (10,000+ ⭐) | `Hardware & Maker Skills` | [PR #747](https://github.com/BehiSecc/awesome-claude-skills/pull/747) |
| **rohitg00/awesome-claude-code-toolkit** (2,300+ ⭐) | `Skills -> Hardware Automation` | Prepared / Active |
| **Prat011/awesome-llm-skills** (1,700+ ⭐) | `3D Printing & Motion Control Skills` | Prepared / Active |
| **libukai/awesome-agent-skills** (5,100+ ⭐) | `精选技能 -> 3D打印与固件调试 (3D Printing & Firmware)` | Prepared / Active |
| **skillmatic-ai/awesome-agent-skills** (670+ ⭐) | `Popular Collections / 3D Printing` | Prepared / Active |
| **philipbankier/awesome-agent-skills** | `Domain-Specific -> Digital Fabrication` | Prepared / Active |
| **karanb192/awesome-claude-skills** | `3D Printing & Embedded Motion` | Prepared / Active |
| **spencerpauly/awesome-cursor-skills** | `Hardware & G-code Calibration` | Prepared / Active |
| **jqueryscript/awesome-claude-code** (510+ ⭐) | `Agent Skills -> Maker Tools` | Prepared / Active |
| **awesome-3d-printing** | `3D printing software, slicers, firmware tools` | Target Catalog |
| **awesome-reprap** | `Open-source 3D printer mechanics, motion control` | Target Catalog |
| **awesome-gcode** | `CNC, 3D printer G-code analysis and post-processors` | Target Catalog |
| **awesome-maker** | `Digital fabrication, CNC milling, FDM tuning` | Target Catalog |
| **awesome-embedded** | `Real-time motor stepping and motion firmware` | Target Catalog |
| **awesome-robotics** | `Kinematics and multi-axis leveling compensation` | Target Catalog |

---

## 3. High-Traffic Launch Channels

### 1. Hacker News (Show HN)
- **Title:** `Show HN: Marlin Bed Leveling – Agent skill for 3D printer mesh ABL/UBL calibration`
- **URL:** `https://wwewtech.github.io/marlin-bed-leveling/`
- **Body:**
  ```text
  Hey HN!

  First-layer failure remains the #1 cause of failed 3D prints. Many hobbyists enable Auto Bed Leveling (G29) but don't realize their start G-code disables leveling or misses Z-probe thermal expansion offsets.

  We built marlin-bed-leveling (https://github.com/wwewtech/marlin-bed-leveling), an open-source agent skill (SKILL.md) for automated Marlin 2.x bed leveling calibration:
  1. Mesh diagnosis: detects bed tilt, taco bowl warp, and eccentric leadscrew binding
  2. G-code workflow audit: verifies G28 homing order, M420 S1 state restore, and Z-fade height
  3. Probe Z-offset calibration mathematics ($Z_{final} = Z_{probe} + \Delta$)
  4. Unified Bed Leveling (UBL) and Bilinear ABL presets with thermal soak timing

  Install via Skills CLI:
  $ npx skills add wwewtech/marlin-bed-leveling
  Or for Claude Code:
  $ claude skills add https://github.com/wwewtech/marlin-bed-leveling

  Interactive 3D mesh viewer: https://wwewtech.github.io/marlin-bed-leveling/
  ```

### 2. Product Hunt
- **Tagline:** `Autonomous calibration agent for Marlin 3D printer bed leveling & G-code`
- **Description:** `Diagnose mesh bed leveling (ABL/UBL), fix first-layer squish, eliminate nozzle scraping, and audit slicer start G-code automatically.`
- **Tags:** `3D Printing`, `Hardware`, `Developer Tools`, `Open Source`, `Makers`.

### 3. Reddit (`r/3Dprinting`, `r/ender3`, `r/prusa3d`, `r/ClaudeAI`)
- **r/3Dprinting:** `Why G29 isn't saving your prints: How Marlin resets mesh leveling after G28 (and how to fix it)`
- **r/ender3:** `Automated start G-code auditor & bed leveling diagnosis tool (open-source agent skill)`
- **r/ClaudeAI:** `[Skill] Marlin Bed Leveling: Stop failed first layers and calibrate ABL/UBL meshes`

### 4. Russian Tech Ecosystem (Хабр & Telegram)
- **Хабр:** «Калибровка стола в Marlin 2.x: почему G29 не спасает первую печать и как автоматизировать ABL/UBL через агентский навык»
- **Telegram:** `@ru_3d_printing`, `@maker_diy`, `@marlin_firmware`, `@neuro_dev`.

---

## 4. Universal 1-Click Installation Cheatsheet

```bash
# 1. skills.sh (Universal Skills CLI)
npx skills add wwewtech/marlin-bed-leveling

# 2. Claude Code
claude skills add https://github.com/wwewtech/marlin-bed-leveling

# 3. Google Antigravity
curl -sL https://raw.githubusercontent.com/wwewtech/marlin-bed-leveling/main/SKILL.md -o ~/.gemini/config/skills/marlin-bed-leveling/SKILL.md

# 4. Cursor (.cursor/rules/ or .cursor/skills/)
mkdir -p .cursor/skills/marlin-bed-leveling
curl -sL https://raw.githubusercontent.com/wwewtech/marlin-bed-leveling/main/SKILL.md -o .cursor/skills/marlin-bed-leveling/SKILL.md

# 5. Windsurf / Cascade
mkdir -p .windsurf/skills/marlin-bed-leveling
curl -sL https://raw.githubusercontent.com/wwewtech/marlin-bed-leveling/main/SKILL.md -o .windsurf/skills/marlin-bed-leveling/SKILL.md
```
