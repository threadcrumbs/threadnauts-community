# Changelog

What changed in each release of Threadnauts. Run `npx @threadcrumbs/threadnauts@latest` to get
the newest one.

## 1.3.0 — November 9, 2026

- **A new look, shared with Threadgauge:** the sidebar, bot cards, settings, help, and toasts take
  the Threadcrumbs theme and its fonts, Inter and JetBrains Mono, so the two apps look like one
  family. The 3D world and its lettering keep their own look.
- **The sidebar is on the left:** it's as wide as Threadgauge's list, the camera buttons move to
  the right edge, and a bot's card opens on the side away from the sidebar. The counts are status
  lamps in order of urgency: Needs you, Error, Done, Working, Waiting on agents, Shipped, then Idle.
  Organizations and repos are headings, and a repo's threads are rows with their status and when
  they last moved.
- **Bot cards:** a card reads like Threadgauge's details, from where the thread lives to its title,
  then its status and what it's doing. The context gauge turns amber at 70% and red at 90%.
- **Live details from Threadgauge:** while Threadgauge runs, a bot's card shows the tool it's
  running and on what, how long its turn has run, which subagents or threads it's waiting on, and
  what it needs from you: a question and its options, a tool waiting for permission, or an error.
  Point at its status to see why it has it. The header and Settings › Threadcrumbs get a button
  that opens Threadgauge. On a phone or another computer on your network, the card leaves out
  questions, commands, and other text.
- **Status colors match Threadgauge's:** Needs you is yellow, Working blue, Waiting on agents
  violet, Done green, Error coral, and Idle a quieter gray, spread in lightness so they stay apart
  in every kind of color vision.
- **Zone and district colors:** six zone colors and four district colors moved off the new status
  colors, so a zone's lights never look like a bot's status. Zones and districts on default colors
  may change color. Colors you picked yourself stay.
- **The Commander's menu:** the pilot's card is now a menu. *Ship* picks your ship, and replaces
  the Ship setting. *Go to…* shows every world as its icon, so you can travel from the ship.
  Prompts and Actions are coming soon. Right-click the ship, or press and hold it, to open the menu
  too. His card holds still while he bobs and scans the view.
- **Organizations:** click one in the sidebar to center its district, the way a repo centers its
  zone.
- **Bots:** a bot walking past the ship's landing legs no longer gets stuck against one, and
  Working and Waiting on agents badges no longer dim as you zoom out.
- **Ports:** Threadnauts no longer starts on a port another app holds only on `::1`, such as a dev
  server on `localhost`, and only a page Threadnauts served on its own port can open threads,
  start conversations, or show folders.

## 1.2.0 — November 6, 2026

- **Twelve ships:** Bug Hunter joins the fleet, a low, crouched tracker with a clamshell tail and a
  striped drop ramp. Zero Day is new with Pro: a long needle nose and one smooth body with its
  engines sculpted in.
- **Race Condition is now a Pro ship:** it's rebuilt as a satin-orange wedge with blade lights, a
  wraparound canopy, and an engine in its nose. Without Pro, a saved Race Condition opens as Thread
  Crosser, and you can pick any of the ten free ships.
- **Ship names:** Core Dumper, Force Pusher, and Hot Fixer are now Core Dump, Force Push, and Hot
  Fix.
- **Ship clicks:** click the hatch to vent steam and open it for a moment. Click anywhere else on
  the ship and its pilot answers and opens his Commander card, where global prompts and actions are
  coming soon. On Race Condition and Zero Day, the space below the elevator counts as the hatch.
- **The pilot keeps watch:** he now scans the view with narrowed eyes.
- **Walls:** zone and district walls now bend with the world, and zone walls stand half as tall as
  district walls. District walls keep their neon colors but glow as strongly as zone walls, and
  walls and names stay as easy to read by day as they are at night.
- **Repo names:** they're lettered like district names now, in the repo's color, without the dot.
- **Saving:** if another program is holding your colony file, Threadnauts now waits and tries again.
  A file it can't read no longer looks like an empty colony.

## 1.1.0 — November 2, 2026

- **Ten ships:** the lander is now one of ten dropships, each with a working hatch, a lit bay,
  steam that purges now and then, and a Baut pilot behind the cockpit glass. Thread Crosser is
  the default. Pick another under View, or right-click the ship. Click the hull to vent steam, or
  the pilot to say hello.
- **Droids:** the cargo drones are now three hovering droids, Ping, Daemon, and Fetch, with a
  soft hum that's easy to live with. They keep clear of whichever ship has landed.
- **Move your bots:** drag a bot to another spot in its zone, or walk the selected bot with the
  arrow keys. Shift runs.
- **Zones:** kerbs lie flush with the deck, walls ripple when a bot passes through, and you can
  change a zone's or district's color from the sidebar. Box piles are cardboard, taped and
  labelled in the repo's color.
- **Bots:** a re-shown zone's bots come back out of the ship, a bot only looks at you when it's
  facing your way, the Error face is sad, and a bot no longer gets stuck walking back to another
  zone's yard.
- **Worlds:** `L` steps through Live too, and fog no longer glows after dark on bright worlds.
  With Pro, Jupiter's Great Red Spot is a storm you sit inside, and Arrakesh has a surprise for
  zones that leave the map.
- **Defaults for new players:** the world curve starts at 25%, and the sound sliders at half,
  with bot voices and machinery at full.

## 1.0.0 — November 1, 2026

The first release.

- **The colony:** every coding-agent thread on your computer as a bot in a 3D colony, one hex
  zone for each repo, grouped into districts by organization.
- **Harnesses:** Claude Code, Codex, OpenCode, Antigravity CLI, Cursor, Hermes, and Kilo Code,
  all at once.
- **Threads:** a bot's card shows its thread, and Open takes you back to it in its harness. `N`
  flies to the next bot waiting on you.
- **Worlds:** eighty of them, with a full day and night. Twenty-four are free.
- **Threadnauts Pro:** opens the other 56 worlds, with one license key for three computers.
- **Your work stays put:** it reads your harnesses' files on your computer, never writes to them,
  and sends nothing about your threads anywhere.
