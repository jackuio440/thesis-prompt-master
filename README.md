# thesis-prompt-master

A Claude Code skill that generates optimized, paste-ready prompts for writing or revising academic theses (Master's and PhD dissertations).

## What it does

When you describe a thesis writing task, this skill produces **one complete Claude prompt** — structured, grounded, and ready to paste into [claude.ai](https://claude.ai). No partial examples. No theory. Just the prompt.

Supports both **Traditional Chinese** (台灣碩博士論文格式) and **English** thesis output.

## Covered chapters

| Chapter | 中文對應 |
|---------|---------|
| Introduction | 緒論 |
| Literature Review | 文獻回顧 |
| Methodology | 研究方法 |
| Results | 研究結果 |
| Discussion | 討論 |
| Conclusion | 結論與建議 |
| Abstract | 摘要 |

Also handles: **revise**, **expand**, **translate/adapt**, and **transition sentences** between sections.

## Key guarantees

- Never fabricates citations, data, or statistics — enforces `[待補]` / `[INSERT VALUE]` placeholders
- Always locks scope to the requested chapter only
- Every prompt includes an explicit output contract (chapter, word count, tense, voice, language)
- Collects format requirements (word count, citation style, heading numbering) and injects them into the prompt automatically
- Bundles all clarifying questions into a single message — never asks one at a time

## Installation

1. Download `SKILL.md`
2. In Claude Code, run:

```
/install SKILL.md
```

## Usage

Describe your task in natural language — the skill detects task type, chapter, and language automatically.

**Examples:**

```
幫我寫碩士論文緒論的 prompt，研究主題是台灣高中生的英語學習動機
```

```
Give me a prompt to write the Methodology chapter for my PhD thesis on urban heat island effects
```

```
幫我修改這段文獻回顧，改善學術語氣
```

## Output format

Every response contains:

1. A single copyable prompt block
2. A one-line description of what the prompt produces
3. A short usage note (only when placeholders need filling)

## License

MIT — see [LICENSE](LICENSE)
