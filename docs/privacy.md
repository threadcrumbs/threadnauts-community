# What stays on your computer

Threadnauts runs on your computer, reads your harnesses' files there, and draws the colony in your
browser. There's no account and no sign-in.

| | |
| --- | --- |
| **Reads** | Your harnesses' own session records and transcripts |
| **Writes** | `colony.json` in its data folder, with your colony's layout and the names and paths of your repos. With Pro, also your license and the downloaded Pro worlds, in the shared Threadcrumbs folder |
| **Never writes** | Anything belonging to a harness. Archiving or hiding a thread here changes nothing in the harness |
| **Sends** | Nothing, without Pro. With Pro: your license key and a random ID for this computer when you activate, then the license itself, to renew it about once a week and to download Pro worlds |
| **Never sends** | Your threads, code, prompts, or project names. There's no telemetry |

## Where it keeps things

| | Data folder | Threadcrumbs folder |
| --- | --- | --- |
| Windows | `%APPDATA%\Threadnauts` | `%APPDATA%\Threadcrumbs` |
| macOS | `~/Library/Application Support/Threadnauts` | `~/Library/Application Support/Threadcrumbs` |
| Linux | `$XDG_DATA_HOME/threadnauts`, or `~/.local/share/threadnauts` | `$XDG_DATA_HOME/threadcrumbs`, or `~/.local/share/threadcrumbs` |

`THREADNAUTS_DATA_DIR` and `THREADCRUMBS_DATA_DIR` move them. `colony.json` holds the names and
paths of the repos you work in, so it's readable by your account only. Every Threadcrumbs app
shares the Threadcrumbs folder, so a license entered in one counts in the others.

## Who can reach it

The server listens on `127.0.0.1`, so nothing outside your computer can reach it. Its API
answers only its own page: a request that names another host, or comes from another website, is
refused. The page runs only its own script, can't be put in a frame, and fetches nothing but
this server.

## Opening threads

**Open** hands a thread to its harness through that harness's own link, which your operating
system passes on. With **Open threads in** set to *Terminal*, it starts the harness's CLI in a
terminal instead. **New conversation** starts an empty thread in a repo's folder, the same way
the harness's own "new session here" action does. Either way, the harness does the opening, and
Threadnauts writes nothing to it.

## Serving it to your network

`THREADNAUTS_HOST` changes the address it listens on, so you can watch the colony from a tablet:

```bash
THREADNAUTS_HOST=0.0.0.0 npx @threadcrumbs/threadnauts
```

If devices reach it by a name or address the server can't see for itself (from WSL2, for
example), list them, comma separated, in `THREADNAUTS_ALLOWED_HOSTS`.

**Know what that hands out before you do it.** There's no password. Anyone who can reach the port
gets every thread title, every opening prompt, every working folder and branch, and the ability
to open threads, reveal folders, and start sessions on your computer. That's fine on a network
you own, and not on café Wi-Fi.
