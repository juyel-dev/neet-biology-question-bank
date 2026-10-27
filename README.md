# NEET Biology Question Bank

NCERT Biology question bank organised **one PDF page at a time**.

## Organisation

- `data/biology/` contains the question data in JSON.
- Each page has its own JSON file.
- `pdf_page` records the page number in the complete PDF.
- `chapter_page` records the page number within a chapter when applicable.
- Unit introductions and other front matter are kept separate from chapter content.
- Every question has a stable ID, question type, options, answer, explanation, source excerpt, difficulty, origin label, and verification status.

## Source and accuracy rules

1. Questions must be grounded in the provided NCERT page.
2. Do not label generated practice questions as actual NEET previous-year questions.
3. Preserve NCERT terminology and meaning.
4. Keep source excerpts short and relevant to the question.
5. Mark a question `reviewed_against_source` only after checking it against that page.
6. Work on one page per content batch; do not silently include material from later pages.

## Current coverage

| PDF page | Section | Status | Questions |
| --- | --- | --- | ---: |
| 1 | Unit 1 introduction — Diversity in the Living World | Added | 24 |

The first two PDF pages are kept as unit front matter. Chapter 1, **The Living World**, begins on PDF page 3 in the supplied PDF.
