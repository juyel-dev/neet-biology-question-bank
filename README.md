# NEET Biology Question Bank

NCERT Biology question bank for **Class 11 and Class 12**, organised one source-PDF page at a time.

## Repository structure

```text
data/
├── class-11/
│   └── biology/
│       ├── unit-01-<unit-slug>/
│       │   ├── unit-introduction/
│       │   │   └── pdf-page-001.json
│       │   └── chapter-01-<chapter-slug>/
│       │       ├── pdf-page-003.json
│       │       └── pdf-page-004.json
│       └── unit-02-<unit-slug>/
└── class-12/
    └── biology/
        └── unit-01-<unit-slug>/
```

### Organisation rules

- Class is the top-level partition: `class-11` or `class-12`.
- Subject is the next level: currently `biology`.
- Keep NCERT units separate using `unit-NN-<unit-slug>`.
- Keep chapter content under `chapter-NN-<chapter-slug>`.
- Unit introductions, prefaces, and other PDF front matter outside a chapter go under `unit-introduction/` or another clearly named section. Do not mislabel them as chapter content.
- Store each PDF page in its own `pdf-page-NNN.json` file. Do not combine multiple pages into one file.
- In each file, `pdf_page` is the page in the complete source PDF; `chapter_page` is the page within the chapter, when applicable.
- Include class, subject, unit, chapter/section, source PDF, and page metadata in every page file.
- Stable question IDs follow `BIO-C11-U01-INTRO-P001-Q001`: class, unit, chapter/section, PDF page, question number. Use `C12` for Class 12.
- If subjects are added later, add a subject folder beside `biology`; do not mix subjects.

## Question data conventions

Each question should include a unique ID, type, topic, question text, options or matching data as appropriate, correct answer, explanation, short source excerpt, difficulty, question origin, and verification status.

- JSON is the canonical structured data format.
- Markdown is for documentation and human-readable guides.
- Do not label generated NCERT-based practice questions as actual NEET previous-year questions.
- Preserve the source's terminology and meaning.
- Keep source excerpts short and relevant to the question.
- Use `reviewed_against_source` only after checking against the specific page.
- Work on one PDF page per batch; do not silently include material from later pages.

## Current coverage

| Class | Subject | Unit / section | Source PDF page | Questions |
| --- | --- | --- | ---: | ---: |
| 11 | Biology | Unit 1 introduction — Diversity in the Living World | 1 | 24 |

In the supplied PDF, pages 1–2 are Unit 1 front matter; Chapter 1, **The Living World**, starts on PDF page 3. Front matter remains in the repository but is separate from Chapter 1.
