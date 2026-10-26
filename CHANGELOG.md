# Changelog

All notable changes to this package are listed here.

## [2.0] - 2026-10-26

### Added
- Shared `ABOUT_ME.md` for the owner's name, time zone, tone, goals, and hard no's. Every bot reads it, and the Command Bot keeps it current.
- `NEW_BOT_TEMPLATE.md`, with required lines, a setup checklist, and a change log. The Command Bot improves it after every setup.
- A Lessons section in every bot's memory file, with a monthly tidy.
- An archive inbox (`Archive/_Inbox/`) and holding folder (`Archive/_Holding/`), filed by the Archive Bot in one weekly batch.
- Keywords on every `MASTER.md` line, and a check of `MASTER.md` before any bot starts a new project.
- Retired-bot records (`Archive/Bots/<BotName>.md`) with 1-5 grades, plus a `BOTS.md` index.
- An "Awaiting archive or delete" section in the weekly review, and a monthly tidy of every bot's description and usage.
- A first-run setup that removes itself when it's done.
- Credit to Robin Delta's (@heyrobinai) Chief of Staff prompt.

### Changed
- Finished projects go to the archive inbox as files instead of being sent to the archivist as messages, and the Archive Bot doesn't reply with "filed" messages.
- The Command Bot's first-run questions now start with a single question about you, and the weekly review day is your choice.
- Common rules (file rules and safety rules) are now identical, word for word, across both bots and every new bot.

## [1.0] - 2026-10-25

### Added
- First version: a Command Bot and an Archive Bot, each pasted into its own description.
