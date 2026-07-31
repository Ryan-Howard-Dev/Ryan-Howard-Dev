# Ryan Howard

I build **Sandbox**: a group of applications that keep your media, your documents and your records
on hardware you own, rather than on a company's servers.

## The problem this addresses

Most consumer software is paid for by what it learns about the people using it. Listening
histories, reading habits, contacts and location are gathered, retained and sold on, and the
service stays useful only for as long as the company continues to operate and the subscription
continues to be paid. When either of those stops, the library goes with it. A collection assembled
over years can be emptied by a licensing dispute the owner never hears about.

Sandbox reverses that arrangement. The files are yours and they remain on your own devices. There
is no account on a server belonging to me, because there is no server belonging to me.

Sandbox supports a single identity, created by you and used across every application in the group,
so that settings, library and listening history follow you between phone, desktop and television.
That identity is held on your own hardware and shared with nobody. It connects your devices to one
another; it does not connect you to me. Nothing is transmitted back to me, so there is nothing for
me to sell, to surrender, or to lose.

## The applications

| Project | What it is | Status |
|---------|-----------|--------|
| [sandbox-audio](https://github.com/Ryan-Howard-Dev/sandbox-audio) | **Sandbox Audio** — a player built on three pillars: music, podcasts and audiobooks. The audiobooks pillar covers reading as well as listening, taking EPUB, PDF, DOCX, HTML, Markdown and plain text and narrating any of them through the device’s own speech engine, so a book or a paper held only as a file can be listened to. It reads M4B chapter marks, regroups recordings split across many files, imports a Calibre library from its folder tree, and searches LibriVox, Project Gutenberg and the Internet Archive. Files are held on the device itself, so playback continues when the connection does not. Runs on Android, Android TV and desktop. | Beta |
| [sandbox-os](https://github.com/Ryan-Howard-Dev/sandbox-os) | **Sandbox OS** — a Debian-based operating system arranged around *stations*. This repository holds the architecture, the decisions behind it, and the specification for each station. | In development |
| [sandbox-builder-docs](https://github.com/Ryan-Howard-Dev/sandbox-builder-docs) | **Sandbox Builder** — the interface and compilation tools that the stations are assembled from. The operator documentation is public; the application source is not. | In development |

### What a station is

A conventional desktop presents a screen of separate programs and leaves the user to work out which
combination performs the task in hand. A station is the task itself, with everything required to
complete it gathered in one place. The specifications published so far cover media, documents,
marketplace, social, mail and video. Each is governed by a written constitution setting out what it
may do, what it may store, and what it must never send elsewhere.

## The Sandbox Server

The applications above can share a single small server that you run at home, on a spare machine, a
home server or a single-board computer. It is described in full in
[TIER34.md](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/TIER34.md), and the
capabilities it does and does not yet have are recorded in
[the capability matrix](https://github.com/Ryan-Howard-Dev/sandbox-os/blob/main/docs/TIER34-FOUNDER-BRIEF.md).

It performs three jobs:

- **It keeps your library consistent across your devices.** Files added on one device become
  available on the others, transferred directly between machines on your own network. Nothing is
  uploaded to an external service on the way.
- **It searches your collection**, so a large library remains usable from a phone without that
  phone holding an index of everything.
- **It lets one device take over from another.** A recording started on a phone can be picked up on
  a desktop or a television at the point it reached.

Everything remains inside your own network. The server is optional: with no server at all, each
application works entirely on its own, and only the transfer between devices is lost.

## In development

A single record of everything listened to and read, held across music, podcasts, audiobooks and
ebooks together rather than as four separate histories that never meet. Every play is recorded
once, appended and never rewritten, so the same record answers a question such as what was finished
last month across every kind of media at once. Each work carries a state -- intended, started,
finished, abandoned, being revisited -- so that a part-read book and a part-heard series behave
alike, and lists can be arranged by hand for the backlog rather than the queue currently playing.
An Insights view draws on that record to show how listening actually falls across the week and
across formats.

Comparable services keep this history on their own servers, where it is retained and analysed. Here
it remains on your hardware. Synchronisation between your own machines through the Sandbox Server is
optional, exporting to Last.fm or ListenBrainz is available if wanted and required by nothing, and
in air-gapped operation no record leaves the device at all. The design is settled; implementation
has not begun.

## Also

**Sandbox Wrestling** is a wrestling promotion simulator written in Godot, with its own match
engine and weekly simulation. It is a separate project rather than part of Sandbox, and it remains
private until it reaches Early Access.

## Documentation

- [Sandbox Audio README](https://github.com/Ryan-Howard-Dev/sandbox-audio#readme) — what the application does, what it does not do, and how to build it
- [BUILDING.md](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/BUILDING.md) — there are no published downloads yet, so it must be built from source
- [Why the library never deletes anything on its own](https://github.com/Ryan-Howard-Dev/sandbox-audio/blob/main/adr/001-locker-never-auto-delete.md) — a decision I was not prepared to compromise
- [Sandbox OS decisions](https://github.com/Ryan-Howard-Dev/sandbox-os/blob/main/docs/DECISIONS.md) — the architectural record
- [Sandbox Server capabilities](https://github.com/Ryan-Howard-Dev/sandbox-os/blob/main/docs/TIER34-FOUNDER-BRIEF.md) — a table marking each capability as working, partial or not started

I write the documentation alongside the code. Every decision that has to hold is recorded briefly
at the point it is made, and each capability is marked as shipped, partial or not started, so that
the documentation can be relied upon to describe the software as it actually is rather than as it
is intended to become.

Everything published here is released under GPL-3.0.
