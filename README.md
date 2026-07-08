# TechCamp Boot Camp

A gated online course site for the TechCamp Boot Camp — an intensive, beginner-friendly
programme covering Ethical Hacking, Arduino & C, and Python. Hosted on GitHub Pages at
**techcamp.live**.

Instructor: Gyamerah Afriyie Philimon · WhatsApp 0554 197 193 · Kumasi, Ghana.

## Design

The site uses an "engineering fieldbook" visual system — a light paper background with a
faint drafting grid, `Space Grotesk` for display, `IBM Plex Sans` for body, and
`JetBrains Mono` for labels and code. Colour is restrained: graphite ink, a pine accent,
and safety-orange used sparingly. Each course track carries its own accent (slate for
Week 1, copper for Week 2, pine for Week 3). Code and consoles sit in dark terminal panels.
There are no emojis anywhere — all iconography is inline SVG.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Login gate — student name + access code |
| `portal.html` | Student hub — progress rings and links to all modules |
| `week1.html` | Module 1 — Ethical Hacking Fundamentals |
| `week2.html` | Module 2 — Arduino & C Programming (live C console via Wandbox) |
| `week3.html` | Module 3 — Python Programming (live Python console via Pyodide) |
| `python-cheatsheet.html` | Searchable, printable Python reference |
| `certificate.html` | Certificate-of-completion generator |
| `bootcamp-poster.html` | Marketing flyer with registration countdown |
| `instructor-guide.html` | Private guide for managing student access (keep unlisted) |

## Access system

Students log in on `index.html` with their registered name and a personal `TC-XXXX` code.
The list of valid students lives in the `STUDENTS` object inside `index.html`. Login state
is held in `sessionStorage`; module progress is saved per student in `localStorage`. See
`instructor-guide.html` for the full workflow.

## Notes

- The live consoles need an internet connection (Wandbox for C, the Pyodide CDN for Python);
  offline they will show a network/load message — this is expected.
- The poster countdown targets `2026-03-31`; update that date in `bootcamp-poster.html`
  for future cohorts.
- `CNAME` maps the GitHub Pages site to `techcamp.live`.
