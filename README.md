# Ryan Howard

I build **Sandbox** — software that runs on hardware you own instead of on someone else's servers.
There are three applications so far, for Linux, Android and the web.

The principle behind all of them is the same. Your music, your books and your files stay on your own
machines. Nothing asks you to create an account, nothing reports back to me, and where something
isn't finished the documentation says so.

## The projects

| Project | What it does | Status |
|---------|-------------|--------|
| [sandbox-audio](https://github.com/Ryan-Howard-Dev/sandbox-audio) | **Sandbox Audio** plays music, podcasts, audiobooks and ebooks. Your files sit on your own device, so it carries on working when the internet doesn't. It runs on Android, Android TV and desktop. | Beta |
| [sandbox-os](https://github.com/Ryan-Howard-Dev/sandbox-os) | **Sandbox OS** is a Debian-based system arranged around whole activities — playing media, handling documents, buying and selling — rather than a screen full of separate programs. This repository holds the architecture and the reasoning behind it. | In development |
| [sandbox-builder-docs](https://github.com/Ryan-Howard-Dev/sandbox-builder-docs) | **Sandbox Builder** is the interface and the build tools behind those activities. The operator guide is public; the source is not. | In development |

All three can share a small server that you run at home. It keeps your library in step across your
devices, handles searching, and lets one device pick up whatever another was playing. None of it
leaves your own network. At the moment that server lives inside Sandbox Audio, where it is
documented in [TIER34.md](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/TIER34.md).
Separating it into a project of its own is planned, but I haven't started that work.

## Also

**Sandbox Wrestling** is a wrestling promotion simulator I am writing in Godot, with a match engine
of its own. It is a separate project rather than part of Sandbox, and it stays private until it
reaches Early Access.

## Worth reading

- [Sandbox Audio README](https://github.com/Ryan-Howard-Dev/sandbox-audio#readme) — what it does, what it doesn't, and how to build it
- [Why the library never deletes anything on its own](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/adr/001-locker-never-auto-delete.md) — one rule I wasn't willing to bend
- [BUILDING.md](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/BUILDING.md) — there are no downloads yet, so you will need to build it yourself
- [Sandbox OS decisions](https://github.com/Ryan-Howard-Dev/sandbox-os/blob/main/docs/DECISIONS.md)
- [What the home server can and cannot do](https://github.com/Ryan-Howard-Dev/sandbox-os/blob/main/docs/TIER34-FOUNDER-BRIEF.md) — a table that says "not started" where that is the truth

I write the documentation next to the code: a short note whenever a decision has to stick, and a
table that keeps what actually works apart from what I have only planned.

Everything public here is released under GPL-3.0.
