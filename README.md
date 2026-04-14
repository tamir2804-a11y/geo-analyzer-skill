# GEO Analyzer Skill

A Claude Cowork skill that analyzes **Generative Engine Optimization (GEO)** for companies in the Israeli market.

## What it does

Give it any market sector in Israel, and it will:
- Find the top 20 companies in that sector
- Research each company's presence across 6 AI engines (ChatGPT, Gemini, Google AI Overview, Claude, Grok, Google Organic)
- Score each company 1-10 per engine with a customizable weighted average
- Identify specific GEO failures and actionable recommendations
- Output a professional Excel (.xlsx) report with conditional formatting

## Installation

**Option A — .skill file:**  
Download the `.skill` file from [Releases](../../releases) and drag it into Cowork.

**Option B — Manual:**  
Copy the `geo-analyzer` folder into your `.claude/skills/` directory.

## Usage

Just tell Claude something like:
- "תעשה ניתוח GEO לסקטור הביטוח"
- "GEO analysis for the Israeli fintech sector"
- "מצב GEO של חברות נדל״ן בישראל"

Claude will ask about score weights and then run the full analysis.

## Output

An Excel file with two sheets:
1. **GEO Analysis** — All 20 companies ranked by weighted score, with color-coded scores, website links, failures, and recommendations
2. **Weights & Methodology** — The scoring weights used and methodology notes

## File Structure

```
geo-analyzer/
├── SKILL.md                        # Skill instructions
└── scripts/
    └── generate_geo_excel.py       # Excel generation script
```

## License

MIT
