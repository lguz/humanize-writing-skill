# Humanize Writing — Claude Code Skill

A skill for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that rewrites AI-generated text to sound like a real human wrote it.

It catches the patterns that make AI writing obvious — the vocabulary, the sentence structures, the too-perfect tone — and fixes them through a systematic 3-pass editing process.

## What It Does

**Pass 1: Kill the AI Vocabulary** — Replaces words like "delve," "leverage," "tapestry," and other statistically overused AI words with simpler human alternatives.

**Pass 2: Break the AI Structures** — Eliminates structural patterns like parallel negation ("Not X, but Y"), tricolons (groups of three), em dash overuse, rhetorical Q+A, and mirror structures.

**Pass 3: Add Human Texture** — Varies sentence length, adds contractions, lets some thoughts stay unresolved, and makes the author's actual opinion visible.

Includes special rules for LinkedIn posts and a 14-point quality checklist.

## Installation

### Option 1: Install from `.skill` file

Download the latest `.skill` file from [Releases](../../releases) and install it:

```bash
claude install-skill humanize-writing.skill
```

### Option 2: Install from this repo

```bash
claude install-skill https://github.com/luisguzman/humanize-writing-skill
```

### Option 3: Manual setup

Copy `SKILL.md` and the `references/` folder into your Claude Code skills directory:

```
~/.claude/skills/humanize-writing/
├── SKILL.md
└── references/
    └── ai-patterns-dictionary.md
```

## Usage

Once installed, Claude Code will automatically use this skill when you say things like:

- "Humanize this text"
- "Make this sound less like AI"
- "This sounds too ChatGPT, fix it"
- "Rewrite this to sound more natural"
- "Clean up this AI-generated draft"

## What's Inside

- **`SKILL.md`** — The main skill definition with the 3-pass rewriting process, LinkedIn-specific rules, and quality checklist
- **`references/ai-patterns-dictionary.md`** — A comprehensive dictionary of AI writing tells: 36+ banned words across 3 tiers, 10 banned structural patterns, tone/voice tells, and content-level red flags

## Writing Philosophy

Based on the idea behind Paul Graham's writing style: clarity over cleverness, directness over decoration. Good writing sounds like a smart person thinking out loud. The goal is invisible editing — the reader should never think about *how* something was written.

## Sources

The AI patterns dictionary draws from:

- [Wikipedia: Signs of AI Writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [GPTZero AI Vocabulary Research](https://gptzero.me/ai-vocabulary)
- [Chris Herbert's ChatGPT Overused Words](https://gist.github.com/chrisgherbert/c734ec50ae464135be57cd03b84281f9)
- [Sabrina Ramonov's Humanizer Prompt](https://github.com/SabrinaRamonov/prompts/blob/main/humanize_ai_writing.md)
- [God of Prompt: 500 ChatGPT Overused Words](https://www.godofprompt.ai/blog/500-chatgpt-overused-words-heres-how-to-avoid-them)

## License

MIT
