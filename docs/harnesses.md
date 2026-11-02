# Harnesses

A **harness** is whatever runs your agent threads: Claude Code, Codex, Cursor, and the rest.
Threadnauts reads each one's own session files, on your computer. It never writes to them.

Every harness you have installed shows up at once, and each bot carries the name of the harness
it belongs to.

## What's supported

| Harness | What Threadnauts reads | What Open does |
| --- | --- | --- |
| **Claude Code** | Desktop app and CLI threads, including worktrees, and which ones are running right now | Opens the thread in the Claude desktop app. On Windows, a thread running in a terminal brings that terminal to the front |
| **Codex** | Desktop, VS Code, and CLI threads, which share one store | Opens the thread through Codex's `codex://` link |
| **OpenCode** | Top-level sessions | OpenCode has no link to a single session, so Open is greyed out. Open the repo and pick the session from OpenCode's list |
| **Antigravity CLI** | Transcripts | Opens the thread through `antigravity://` |
| **Cursor** | Agent transcripts. Composer and sidebar threads aren't read yet | Cursor has no link to a single thread, so Open opens the repo in Cursor, where you pick it from the agent list |
| **Hermes** | Sessions for each profile | No Open button. Hermes threads live in the terminal and chat apps, with nothing to link to |
| **Kilo Code** | Top-level sessions | Opens the repo folder in VS Code |

On Linux with no desktop app to answer the link, a terminal opens with the harness's CLI resuming
the thread instead. To always use a terminal, set **Open threads in** to *Terminal* in settings.

## Where each one keeps its threads

These are the default locations. If you moved a harness's data with its own setting, Threadnauts
follows the same setting.

| Harness | Location | Moved with |
| --- | --- | --- |
| Claude Code | `~/.claude/projects` and `~/.claude/sessions`, plus the desktop app's own records | `CLAUDE_CONFIG_DIR` |
| Codex | `~/.codex` | `CODEX_HOME` |
| OpenCode | `~/.local/share/opencode/opencode.db` (on macOS, also `~/Library/Application Support/opencode`) | `OPENCODE_DB` or `XDG_DATA_HOME` |
| Antigravity CLI | `~/.gemini/antigravity-cli` | `ANTIGRAVITY_HOME` |
| Cursor | `~/.cursor/projects` | |
| Hermes | `~/.hermes`, or `%LOCALAPPDATA%\hermes` on Windows, with one store per profile | `HERMES_HOME` |
| Kilo Code | `~/.local/share/kilo/kilo.db` | `KILO_DB` or `XDG_DATA_HOME` |

`~` is your home folder, which is `C:\Users\<you>` on Windows.

## Not yet supported

Amp, Aider, Goose, Qwen Code, and Amazon Q Developer CLI aren't read yet. If you use one of
these, or another harness, [ask for it](https://github.com/threadcrumbs/threadnauts-community/issues/new?template=harness.yml).
If someone has already asked, a 👍 on their request helps us see what to add next. Telling us
where the harness keeps its sessions, and which version you run, makes it much faster to add.

Some of these readers were built from a harness's source code or documented formats and tested
against fake installs, not a real one. If one shows something wrong,
[report it](https://github.com/threadcrumbs/threadnauts-community/issues/new?template=bug.yml)
with the harness's version.
