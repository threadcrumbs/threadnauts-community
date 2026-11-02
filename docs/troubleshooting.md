# Troubleshooting

If none of these fit, [ask in Discussions](https://github.com/threadcrumbs/threadnauts-community/discussions/categories/q-a)
or [report a bug](https://github.com/threadcrumbs/threadnauts-community/issues/new?template=bug.yml).

## A repo isn't on the map

A repo where every thread has been quiet for three days folds away, so a computer with a lot of
checkouts doesn't fill up with empty zones. It's still in the panel's list, dimmed, with a
**Show** button, and it comes back by itself the moment one of its threads wakes up. To keep
every repo on the map, turn off **Hide dormant repos** in settings (`S`).

A repo you hid yourself stays in the same list, with an eye icon and a **Show** button.

## A harness's threads don't show up

1. Check that the harness is [supported](harnesses.md), and that it keeps its threads in the
   usual place. If you moved them with the harness's own setting, set the same variable for
   Threadnauts too.
2. Ask Threadnauts which harnesses it found. With the colony running, open
   `http://127.0.0.1:5274/api/harnesses` in your browser, or run:

   ```bash
   curl -s http://127.0.0.1:5274/api/harnesses
   ```

   Each harness is listed with whether it was detected. Use your port if it isn't 5274.
3. If the harness is detected and threads are still missing,
   [report a bug](https://github.com/threadcrumbs/threadnauts-community/issues/new?template=bug.yml)
   and paste that list.

## Open does nothing

Open hands the thread to its harness's own app, through a link your operating system passes on.
If the app isn't installed, nothing answers the link. For example, a Claude Code thread opens in
the Claude desktop app, so the button needs the Claude app installed even if you start threads
from the CLI.

- **Install the harness's app**, or
- **Use a terminal instead.** Set **Open threads in** to *Terminal* in settings, and Open runs
  the harness's CLI, resuming the thread there. The CLI has to be installed.

Some harnesses have no link to a single thread. See the *What Open does* column in
[harnesses.md](harnesses.md).

## Another app is already on port 5274

Threadnauts takes the next free port and says which one in the terminal. To pick one yourself:

```bash
npx @threadcrumbs/threadnauts --port 5300
```

## It runs slowly, or the fan spins up

Open settings (`S`) and pick a lower **Quality preset**. A fresh install starts on *Balanced*.
**Adaptive quality**, which is on by default, lowers the render scale by itself when frames get
expensive.

## Pro worlds are still locked

- Enter your license key in settings, under **Threadnauts Pro**. It's in your Polar receipt and
  starts with `THREADCRUMBS-`.
- The first time, Threadnauts needs the internet, to add this computer to your license and
  download the Pro worlds. After that, it checks the license on your computer.
- One key works on three computers. If all three are used, remove one in the
  [customer portal](https://threadcrumbs.io/portal).

More in [pro.md](pro.md).

## Getting the newest version

`npx` can keep using a copy it already downloaded. Ask for the latest one:

```bash
npx @threadcrumbs/threadnauts@latest
```

If you installed it with `npm install -g @threadcrumbs/threadnauts`, run that again.

## Watching the colony from a tablet or another computer

Threadnauts only answers your own computer by default. `THREADNAUTS_HOST=0.0.0.0` opens it to your
network. **Read [privacy.md](privacy.md#serving-it-to-your-network) first:** there's no password,
and anyone who can reach the port can see your threads and open them.
