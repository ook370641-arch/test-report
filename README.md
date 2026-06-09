# Work Skill for Claude Code

A Claude Code skill for **task kickoff** and **structured review**.

---

## What it does

This skill only intervenes at two moments:

1. **Kickoff**: Locks in a verifiable task definition (MVP) before you start, writing it to `工作计划*.md` in the project directory.
2. **Closeout**: Reads historical records, compares decision chains, identifies blind spots, and outputs feedforward rules — appended to the same file.

**It does NOT do**: daily to-do lists, time planning, or execute specific technical tasks.

---

## Triggers

- `work`
- `帮我规划一下` / `帮我复盘`
- `想启动新项目` / `遇到了瓶颈`
- `前馈` / `工作复盘`

---

## Files

```
.
├── work/
│   ├── SKILL.md                    # Entry skill (kickoff + review)
│   └── references/
│       └── work-review.md          # 4-phase review protocol
└── README.md
```

---

## Installation

```bash
# Global
cp -r work ~/.claude/skills/

# Project-level
cp -r work ./.claude/skills/
```

---

## Configuration

Replace `{{HISTORY_DIR}}` in `work/references/work-review.md` with your actual historical records directory (e.g. `~/Documents/工作/`), used for cross-project comparison.

---

## Disclaimer

- All skills are in Claude Code format (YAML frontmatter + Markdown), not compatible with other AI assistant frameworks.
