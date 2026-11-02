# Media

The pictures and videos the README and docs use.

| File | What it is | Made with |
| --- | --- | --- |
| `threadnauts-icon.svg` | The app icon | Copied from threadnauts.io |
| `threadnauts-icon-light.svg` | The app icon for light pages, without its dark tile | `threadnauts-icon.svg` with the tile taken out, so the black outlines carry the shape on white |
| `colony.webp`, `thread-card.webp`, `world-*.webp` | Screenshots of the app | The screenshot tool in the threadcrumbs.io site repo (`tools/screenshots`), which runs the app on a made-up home folder of demo threads |
| `install.gif` | The install command in a terminal. Not recorded yet | [VHS](https://github.com/charmbracelet/vhs), from `install.tape` |

Every picture shows demo threads, never real ones. Re-shoot them whenever the app's look
changes, so the README never shows an older version than the one people install.

## The install clip

`install.tape` types the install command and shows what Threadnauts prints. With VHS
installed, from this repo's root:

```bash
vhs media/install.tape
```

Before it starts filming, it sets a made-up data folder, so your own folder names don't end up in
the clip, and has `npx` download the package, so the clip doesn't stop to ask. Stop any
Threadnauts that's already running before you record, or the clip says so instead of starting
one.
