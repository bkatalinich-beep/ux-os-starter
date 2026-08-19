# UX-OS starter

A lightweight operating system for design leadership work: a plain folder of markdown files where your decisions, initiative context, and team knowledge accumulate in one place. The pattern is adapted from the PM-OS idea that has been circulating in product circles (Aakash Gupta's writeup is at news.aakashg.com/p/pm-os), trimmed down to the pieces that earn their keep for a design manager.

You do not need any special tooling. Markdown files in a folder work fine on their own, and they get more useful if you point an AI assistant at them, because everything it needs to help you is written down in one place.

## The layout

- [decisions.md](decisions.md) is the decision registry, and it is the reason this starter exists. Start here.
- [context-library/](context-library/) holds stable context that rarely changes: your product area, your design principles, who your stakeholders are and what they care about.
- [data/projects/](data/projects/) holds one folder per initiative, named with a date prefix like `2026-08-tab-groups`, so the archive stays chronological. Each initiative gets a brief and accumulates its drafts and research over time.
- [templates/](templates/) holds reusable document skeletons. It ships with the design brief; add your own as patterns emerge.

## How to start

Copy this folder, rename it for yourself, and spend an afternoon on three things. Write down the last consequential decision your team made as your first registry entry, even if it happened weeks ago. Create one initiative folder for the biggest thing currently in flight and fill in its brief. Then jot two or three paragraphs of stable context into the context library. That is enough; the system grows from use, and a thin version you actually maintain beats a complete one you abandon.

## Using it with an AI assistant

The kit ships with a skill at [.claude/skills/log-decision/](.claude/skills/log-decision/SKILL.md) that Claude Code picks up automatically when you open the folder. Paste your meeting notes or a Slack thread and ask it to log what was decided; it extracts the entry in the registry format, holds the quality bar on each field (it will push back on a vague revisit clause instead of writing a useless one), and skips things that were discussed without being settled. It can also scan the registry and flag entries whose revisit conditions look triggered. If you use a different assistant, the SKILL.md file reads as plain instructions you can hand it.

## One rule that matters

Keep anything about individual people's performance, 1:1 notes, or unresolved sensitive conversations out of folders you might ever share. If you want to keep people notes at all, give them their own clearly private home and never mix them into initiative folders.
