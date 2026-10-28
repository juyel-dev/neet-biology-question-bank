# NEET PCB Question Bank

NCERT-based question bank for **NEET Physics, Chemistry and Biology** (Class 11 and Class 12), organised one source-PDF page at a time.

## Repository structure

```text
data/
├── class-11/
│   ├── physics/
│   ├── chemistry/
│   └── biology/
│       ├── unit-01-<unit-slug>/
│       │   ├── unit-introduction/
│       │   │   └── pdf-page-001.json
│       │   └── chapter-01-<chapter-slug>/
│       │       ├── pdf-page-003.json
│       │       └── pdf-page-004.json
│       └── unit-02-<unit-slug>/
└── class-12/
    ├── physics/
    ├── chemistry/
    └── biology/
schemas/
└── page-questions.schema.json
```

Path pattern: `data/class-{11|12}/{physics|chemistry|biology}/unit-NN-<slug>/chapter-NN-<slug>/pdf-page-NNN.json`

### Organisation rules

- Class is the top-level partition: `class-11` or `class-12`.
- Subject is the next level: `physics`, `chemistry` or `biology`. Never mix subjects in one folder.
- Keep NCERT units separate using `unit-NN-<unit-slug>`.
- Keep chapter content under `chapter-NN-<chapter-slug>`.
- Unit introductions, prefaces, and other PDF front matter outside a chapter go under `unit-introduction/` or another clearly named section. Do not mislabel them as chapter content.
- Store each PDF page in its own `pdf-page-NNN.json` file. Do not combine multiple pages into one file.
- In each file, `pdf_page` is the page in the complete source PDF; `chapter_page` is the page within the chapter, when applicable.
- Include class, subject, unit, chapter/section, source PDF, and page metadata in every page file.
- Stable question IDs follow `<SUBJ>-C<class>-U<unit>-<CH|INTRO><nn>-P<pdf page>-Q<number>`, e.g. `BIO-C11-U01-CH01-P003-Q001`.
  - Subject codes: `PHY` (Physics), `CHE` (Chemistry), `BIO` (Biology).
  - Class codes: `C11`, `C12`.
- Validate every page file against `schemas/page-questions.schema.json`.

## Question data conventions

Each question should include a unique ID, type, topic, question text, options or matching data as appropriate, correct answer, explanation, short source excerpt, difficulty, question origin, and verification status.

- JSON is the canonical structured data format.
- Markdown is for documentation and human-readable guides.
- Do not label generated NCERT-based practice questions as actual NEET previous-year questions.
- Preserve the source's terminology and meaning.
- Keep source excerpts short and relevant to the question.
- Use `reviewed_against_source` only after checking against the specific page.
- Work on one PDF page per batch; do not silently include material from later pages.
- Physics/Chemistry numericals: state units and show the working in `explanation`.

## Current coverage

| Class | Subject | Unit / chapter | Source PDF | PDF pages | Questions |
| --- | --- | --- | --- | ---: | ---: |
| 11 | Biology | Unit 1 front matter | kebo101.pdf | 1–2 | 36 |
| 11 | Biology | Unit 1, Chapter 1 — The Living World | kebo101.pdf | 3–9 | 135 |
| 11 | Biology | Unit 1, Chapter 2 — Biological Classification | kebo102.pdf | 1–13 | 232 |

Physics (11, 12), Chemistry (11, 12) and Biology (12) folders are set up and waiting for content.

In `kebo101.pdf`, pages 1–2 are Unit 1 front matter; Chapter 1, **The Living World**, starts on PDF page 3. In `kebo102.pdf`, PDF page 1 is the Chapter 2 opener (printed page 10) and PDF page 13 holds the chapter exercises (printed page 22). Front matter remains in the repository but is separate from chapter content.
