# Ryan Howard

I build **Sandbox**, a set of local-first applications for Linux, Android and the web. They keep
your library on hardware you own, they run without an account, and they state plainly which parts
are unfinished.

## Sandbox

| Project | What it is | Status |
|---------|-----------|--------|
| [sandbox-audio](https://github.com/Ryan-Howard-Dev/sandbox-audio) | **Sandbox Audio** plays music, podcasts, audiobooks and ebooks from a locker held on your own device. It runs on Android, Android TV and desktop, and it works with the network switched off. | Beta; builds on device |
| [sandbox-os](https://github.com/Ryan-Howard-Dev/sandbox-os) | **Sandbox OS** is a Debian-based system organised around *stations* rather than a desktop of loose applications. This repository holds the architecture, the decisions behind it, and the station map. | In development |
| [sandbox-builder-docs](https://github.com/Ryan-Howard-Dev/sandbox-builder-docs) | **Sandbox Builder** is the stations interface and its compile toolchain. The operator documentation is public; the application source is not. | In development |

The **Sandbox Server** is the shared household backend. It handles locker synchronisation, search,
and the mirroring of playback state between your own devices across your own network. At present it
ships inside sandbox-audio, where it is documented in
[TIER34.md](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/TIER34.md). Extracting it
into a package of its own is planned, but that work has not begun.

## Also

**Sandbox Wrestling** is a territory booking simulator built in Godot 4.5, with its own match engine
and weekly simulation. It is a separate product rather than part of the platform above, and it
remains private until its Early Access release.

## Worth reading

- [Sandbox Audio README](https://github.com/Ryan-Howard-Dev/sandbox-audio#readme) — what the application does, what it does not, and how to build it
- [ADR: the locker never auto-deletes](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/adr/001-locker-never-auto-delete.md) — a rule that had to hold
- [BUILDING.md](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/BUILDING.md) — how to build it yourself; there are no published releases yet
- [Sandbox OS decisions](https://github.com/Ryan-Howard-Dev/sandbox-os/blob/main/docs/DECISIONS.md)
- [Sandbox Server founder brief](https://github.com/Ryan-Howard-Dev/sandbox-os/blob/main/docs/TIER34-FOUNDER-BRIEF.md) — a capability matrix that marks a feature "not started" when that is the truth

I keep the documentation beside the work: short architecture records when a rule has to hold, and a
capability matrix that separates what has shipped from what is merely planned.

Everything public here is licensed under GPL-3.0.
