# Claude Code Skills

A collection of Claude Code skills for rigorous work: evaluating reports, designing prompts, and structuring tasks.

---

## Skills

### 1. report-review — Evaluation Report Review

Rigorously reviews evaluation reports before they drive decisions.

**What it does:**

Checks whether a report is actually deliverable — not whether it looks complete. Reviews along two axes:

1. **Intuitive credibility**: Can a reader quickly locate the main claim, strongest evidence, key controls, and conclusion boundaries?
2. **Analytical depth**: Have observations been pushed from phenomena to causes, mechanisms, boundaries, and actionable strategy?

**When to use:**

- A/B tests and comparisons
- Prompt / model evaluations
- Quality-assurance and auto-evaluation reports
- Bad-case and failure-mechanism analyses
- Solution adoption / go-no-go decisions
- Daily progress updates that need to freeze a decision

**What it does NOT do:**

- Does not polish style or grammar
- Does not summarize the report for you
- Does not approve a report just because it looks structured

**Files:**

- `report-review/SKILL.md` — main skill reference
- `report-review/references/` — specialized review guides:
  - `solution-decision-report.md`
  - `evaluator-reliability-report.md`
  - `failure-mechanism-report.md`
  - `comparative-quality-report.md`
  - `safety-critical-system-report.md`

---

### 2. work — Task Kickoff & Structured Review

Only intervenes at two moments: task kickoff and closeout.

**What it does:**

1. **Kickoff**: Locks in a verifiable task definition (MVP) before you start, writing it to `工作计划*.md` in the project directory.
2. **Closeout**: Reads historical records, compares decision chains, identifies blind spots, and outputs feedforward rules — appended to the same file.

**It does NOT do**: daily to-do lists, time planning, or execute specific technical tasks.

**Triggers:**

- `work`
- `帮我规划一下` / `帮我复盘`
- `想启动新项目` / `遇到了瓶颈`
- `前馈` / `工作复盘`

**Files:**

- `work/SKILL.md` — entry skill (kickoff + review mode)
- `work/references/work-review.md` — 4-phase review protocol (action chain → historical comparison → blindspot identification → feedforward rules)

---

## File Structure

```
.
├── report-review/
│   ├── SKILL.md
│   └── references/
│       ├── comparative-quality-report.md
│       ├── evaluator-reliability-report.md
│       ├── failure-mechanism-report.md
│       ├── safety-critical-system-report.md
│       └── solution-decision-report.md
├── work/
│   ├── SKILL.md
│   └── references/
│       └── work-review.md
└── README.md
```

---

## Installation

```bash
# Global installation
cp -r report-review work ~/.claude/skills/

# Project-level installation
cp -r report-review work ./.claude/skills/
```

---

## Configuration

Replace `{{HISTORY_DIR}}` in `work/references/work-review.md` with your actual historical records directory (e.g. `~/Documents/work/`), used for cross-project comparison.

---

## Disclaimer

- All skills are in Claude Code format (YAML frontmatter + Markdown), not compatible with other AI assistant frameworks.
