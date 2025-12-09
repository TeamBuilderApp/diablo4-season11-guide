# Contributing to Diablo 4 Season 11 Guide

Thank you for your interest in contributing to this Diablo 4 Season 11 guide! This document provides guidelines for contributing to ensure consistency and quality across all content.

## Table of Contents
1. [Getting Started](#getting-started)
2. [Content Guidelines](#content-guidelines)
3. [TO-VERIFY Placeholders](#to-verify-placeholders)
4. [Formatting Standards](#formatting-standards)
5. [Sources and Attribution](#sources-and-attribution)
6. [Submission Process](#submission-process)

---

## Getting Started

### Prerequisites
- Knowledge of Diablo 4 Season 11 mechanics
- Access to reliable community resources (Maxroll, Icy Veins, Wowhead, Fextralife, AOEAH)
- GitHub account for pull requests
- Text editor with UTF-8 and LF line ending support

### Repository Structure
```
diablo4-season11-guide/
├── classes/              # Class-specific build guides
│   ├── necromancer.md
│   ├── sorcerer.md
│   ├── template.md      # Template for new class guides
│   └── index.md         # Index of all classes
├── docs/                 # Documentation for GitHub Pages
│   ├── _config.yml      # Jekyll configuration
│   ├── _layouts/        # Page layouts
│   ├── _includes/       # Reusable components
│   ├── assets/css/      # Stylesheets
│   ├── classes/         # Class guides for Pages
│   └── index.md         # Site landing page
├── .github/             # GitHub templates
│   ├── ISSUE_TEMPLATE/
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── workflows/
├── CONTRIBUTING.md      # This file
└── README.md            # Repository overview
```

---

## Content Guidelines

### Build Guide Structure
All class build guides should follow this structure:

1. **Overview** - Brief introduction to the class and builds covered
2. **Build Section(s)** - One or more build archetypes with:
   - Core Concept
   - Key Legendary Items
   - Critical Affixes by Gear Slot
   - Numeric Targets
   - Skill Tree Allocation
   - Paragon Board Priority
   - Gameplay Tips
3. **Leveling Guide** - 1-50 progression
4. **Endgame Content Strategy** - Nightmare Dungeons, Pit, Boss Farming
5. **Stat Priority Summary** - Quick reference for gearing

### Writing Style
- **Clarity First:** Write for players of all experience levels
- **Be Specific:** Provide exact values, percentages, and item names
- **Stay Current:** Reference Season 11 data only
- **Avoid Jargon:** Explain abbreviations on first use (e.g., "Damage Reduction (DR)")
- **Action-Oriented:** Use active voice and imperative mood for instructions

### Required Information
Each build must include:
- ✅ Complete legendary item list with effects
- ✅ Affix priorities for all gear slots (helm, chest, gloves, pants, boots, amulet, rings)
- ✅ Numeric targets for offense, defense, and utility stats
- ✅ Skill tree with allocation points
- ✅ Paragon board routing
- ✅ Gameplay tips and rotation advice

---

## TO-VERIFY Placeholders

### Purpose
`TO-VERIFY` placeholders mark data that requires verification against current patch values. This ensures transparency about provisional data.

### Usage Guidelines
Use `TO-VERIFY` when:
- Exact numeric values are unknown (e.g., "TO-VERIFY% damage")
- Patch notes have changed values since last update
- Community consensus is unclear
- Multiple sources report different values

**Examples:**
```markdown
✅ Good: Critical Strike Chance (TO-VERIFY%)
✅ Good: Deals TO-VERIFY% increased damage
✅ Good: Restores TO-VERIFY Mana per second
❌ Bad: Critical Strike Chance (45%) [if not verified]
❌ Bad: Deals more damage [too vague]
```

### Verification Process
To verify a `TO-VERIFY` value:
1. Check the official Diablo 4 patch notes
2. Cross-reference with at least 2 community sources:
   - Maxroll.gg
   - Icy Veins
   - Wowhead
   - Fextralife
   - AOEAH
3. Test in-game if possible
4. Replace `TO-VERIFY` with verified value
5. Note verification date in commit message

### Tracking TO-VERIFY Items
Before merging any PR:
- [ ] List all `TO-VERIFY` placeholders in PR description
- [ ] Assign priority (High/Medium/Low) to each
- [ ] Create follow-up issues for high-priority verifications

---

## Formatting Standards

### File Format
- **Encoding:** UTF-8 without BOM
- **Line Endings:** LF (Unix-style `\n`)
- **Indentation:** 2 spaces (not tabs)
- **Max Line Length:** 120 characters (soft limit)

### Markdown Conventions
- Use `#` for top-level headers (one per document)
- Use `##` for major sections
- Use `###` for subsections
- Use `####` for detailed breakdowns
- Use **bold** for emphasis and item names
- Use `code blocks` for commands or technical terms
- Use `---` for horizontal rules between major sections

### Numeric Formatting
- Percentages: Include `%` symbol (e.g., "45%", not "45 percent")
- Large numbers: Use commas for thousands (e.g., "25,000", not "25000")
- Decimals: Maximum 2 decimal places (e.g., "3.25%", not "3.253%")
- Ranges: Use hyphen without spaces (e.g., "40-50%", not "40 - 50%")

---

## Sources and Attribution

### Approved Sources
All information must come from reputable community sources:

1. **Maxroll.gg** - Build guides, tier lists, planner tools
2. **Icy Veins** - Comprehensive guides and theorycrafting
3. **Wowhead** - Database and news
4. **Fextralife** - Wiki and video guides
5. **AOEAH** - Item database and trading insights

### Citation Format
At the top of each guide, include:
```markdown
**Sources:** Maxroll, Icy Veins, Wowhead, Fextralife, AOEAH
```

---

## Submission Process

### Before Submitting
1. **Read Existing Content:** Familiarize yourself with current guides
2. **Check Open Issues:** Ensure your contribution addresses an open issue or fills a gap
3. **Verify TO-VERIFY Status:** Mark all unverified data clearly
4. **Test Formatting:** Verify UTF-8 encoding and LF line endings
5. **Use the Template:** See `classes/template.md` for class guides

### Creating a Pull Request

#### Branch Naming
Use descriptive branch names:
- `add/<feature>` - For new content (e.g., `add/barbarian-guide`)
- `update/<feature>` - For updates (e.g., `update/necromancer-stats`)
- `fix/<issue>` - For bug fixes (e.g., `fix/typo-sorcerer`)

#### Commit Messages
Follow conventional commit format:
```
<type>: <description>

[optional body]
```

**Types:**
- `feat:` - New feature or content
- `fix:` - Bug fix or correction
- `docs:` - Documentation changes
- `style:` - Formatting changes

**Examples:**
```
feat: Add barbarian build guide with legendary items

fix: Correct necromancer Blood Surge damage values
```

---

## GitHub Pages Setup

After merging content changes, maintainers should enable GitHub Pages:

1. Go to repository **Settings**
2. Navigate to **Pages** section
3. Set **Source** to "Deploy from a branch"
4. Select branch: `main`
5. Select folder: `/docs`
6. Click **Save**
7. Access site at: `https://TeamBuilderApp.github.io/diablo4-season11-guide/`

---

## Questions and Support

### Where to Ask
- **General Questions:** Open a GitHub Discussion
- **Bug Reports:** Open a GitHub Issue with `bug` label
- **Feature Requests:** Open a GitHub Issue with `enhancement` label

---

## License
By contributing, you agree that your contributions will be licensed under the same license as the project (see LICENSE file).

---

## Thank You!
Your contributions help the Diablo 4 community. Whether you're fixing a typo or writing a complete build guide, your effort is appreciated! 🎮⚔️
