# Shared Folder Layout

Both bots use the same file paths inside one shared cloud folder, called `[Bot Files]` in the templates. This page lists every file and folder, who keeps it, and what goes in it.

## Contents

- [Files and folders](#files-and-folders)
- [Tree view](#tree-view)
- [Memory file layout](#memory-file-layout)
- [How a project moves through the archive](#how-a-project-moves-through-the-archive)

## Files and folders

- `[Bot Files]/ABOUT_ME.md` is about [Owner]: name, time zone, tone, goals, hard no's. Every bot reads it. The Command Bot keeps it current when [Owner] corrects a preference.
- `[Bot Files]/TEAM.md` is the roster. The Command Bot keeps it.
- `[Bot Files]/NEW_BOT_TEMPLATE.md` is what every new bot is built from. The Command Bot creates and improves it.
- `[Bot Files]/Memory/mem_<BotName>.md` is one per bot, the Command and Archive bots included: header, Status, Lessons, Notes. Old lines move to `mem_<BotName>_old.md`.
- `[Bot Files]/Archive/_Inbox/<BotName>_<Project>.md` is where any bot drops a finished project: project name, bot name, done date, and final setup details (notes, logs, paths, settings).
- `[Bot Files]/Archive/MASTER.md` is the searchable master list and the record of what's filed. The Archive Bot keeps it.
- `[Bot Files]/Archive/<Category>/<ProjectName>.md` holds one file per archived project.
- `[Bot Files]/Archive/_Holding/` holds anything waiting on the owner's archive-or-delete call.
- `[Bot Files]/Archive/Bots/<BotName>.md` holds one record per retired bot; `Archive/Bots/BOTS.md` lists them with 3-5 keywords each. The Command Bot keeps both.

## Tree view

```text
[Bot Files]/
├── ABOUT_ME.md               # about the owner; every bot reads it
├── TEAM.md                   # roster; kept by the Command Bot
├── NEW_BOT_TEMPLATE.md       # what every new bot is built from
├── Memory/
│   ├── mem_<BotName>.md      # one per bot: header, Status, Lessons, Notes
│   └── mem_<BotName>_old.md  # old lines moved out during the monthly tidy
└── Archive/
    ├── MASTER.md             # searchable master list; kept by the Archive Bot
    ├── _Inbox/               # finished projects waiting to be filed
    ├── _Holding/             # items waiting on the owner's archive-or-delete call
    ├── <Category>/
    │   └── <ProjectName>.md  # one file per archived project
    └── Bots/
        ├── BOTS.md           # retired bots, 3-5 keywords each
        └── <BotName>.md      # one record per retired bot
```

## Memory file layout

Every bot, the Command and Archive bots included, keeps one memory file at `[Bot Files]/Memory/mem_<BotName>.md`:

- **Header:** owner bot, role, created date, and "only the owner bot writes; other bots may read; [Owner] may edit or delete".
- **Status:** exactly these headings: Active, Waiting on [Owner], Finished (recent projects already in `Archive/_Inbox/`), Last updated.
- **Lessons:** one short line each time the owner corrects the bot or it learns what works, what fails, or a tool or setting worth reusing.
- **Notes:** reference the bot builds up (settings, dial-ins, how-tos). Reference is never trimmed or archived.

## How a project moves through the archive

1. A bot finishes a project and saves a short file to `Archive/_Inbox/<BotName>_<Project>.md`: project name, bot name, done date, and final setup details. It doesn't message the Archive Bot.
2. Once a week the Archive Bot files the inbox. Each project becomes `Archive/<Category>/<ProjectName>.md` as numbered steps, with the important notes kept.
3. The Archive Bot adds one line to `MASTER.md`: project name, one-line summary, 3-5 keywords, done date, and a link.
4. Before starting a new project, any bot checks `MASTER.md` for a similar one and reuses its setup.
5. Anything waiting on the owner's archive-or-delete call sits in `Archive/_Holding/`. Nothing is removed for good without the owner's yes.

---

[Back to README](../README.md)
