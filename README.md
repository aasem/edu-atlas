# Atlas of Educational Philosophy

Sixty-five texts on education from India, China, Islam, Judaism and Christianity, Greece, Rome and the Renaissance, and modernity, each read through one governing question:

> What kind of being does education presume the learner to be, and given that being, is education the formation of a person or the transmission of knowledge, toward what end, and on whose authority?

Each text answers seven questions: anthropology, purpose, motive, scope, authority, work and the machine. The Big Picture sets the questions against the six traditions on one chart and opens onto every page.

The atlas has a companion, [Taʿlīm in the Subcontinent](https://aasem.github.io/subcont-edu/), which follows what became of these answers in the subcontinent's schools. Where a text appears in both atlases, the entry links to the other reading.

## What is in the repository

- `index.html` — the reader: its styles, the page shell and the code
- `data/frame.js` — the traditions, the seven questions and their classifications, the essays and closing pages, key words, short names and name links
- `data/entries-*.js` — the entries, one file per tradition
- `data/chart.js` — the Big Picture's cells and routes
- `readings.js` — the reader's own reading of each entry; write in it directly, or write on the page and use **Copy readings.js**
- `big-picture.png` — the chart as an image

## Editing an entry

Each entry is a JavaScript object. The fields are:

| Field | Meaning |
|---|---|
| `n`, `t`, `home`, `d`, `era` | name, tradition, home within modernity (if any), date as shown, period |
| `by`, `wk` | author, and the encyclopedia article the title links to |
| `mn`, `es`, `mo`, `sc`, `au`, `f` | the classifications: nature, where the end comes from, motive, scope, authority, formation or transmission (codes listed in `data/frame.js`) |
| `read`, `tr`, `ol` | passages to read, a translation, and free texts online |
| `ta` | the matching entry in Taʿlīm in the Subcontinent, if any |
| `w` | the work and its setting |
| `p`, `e`, `x`, `mv`, `scp`, `k`, `wo`, `mc` | the answers in prose: 1 anthropology, 2 purpose, what is passed on, 3 motive, 4 scope, 5 authority, 6 work, 7 the machine. The first sentence of each appears on the question pages |
| `o` | the strongest objection |
| `v` | what still needs checking against the primary text |

The page reads the data files directly, so an edit appears on the next reload. No build step is needed. Keep each entry's `n` unchanged, since `readings.js` and the chart refer to entries by name.

## Verification

Passage numbers follow the translations named in each entry, and some differ between editions. Where an entry carries a specific doubt about a passage, a date or a quotation, it is noted under *To verify* and should be checked before citing. The classifications and the chart's one-line summaries are interpretations, meant to be contested in the readings.

© 2026 Asim D. Bakhshi. Text and readings: CC BY 4.0. Code: MIT.
