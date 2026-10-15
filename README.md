# FolioCheck

**Resume & Project Portfolio Parser for Students**

FolioCheck scans a student's resume, project report or lab report, highlights missing requirements, and gives constructive suggestions on structure. It runs entirely in the browser, so nothing a student pastes is uploaded anywhere.

Built for **IBM SkillsBuild Masterclass 5: Creating Real Life Projects**.

![Home screen](docs/screenshots/home.png)

## The problem

Student documents are often submitted with avoidable gaps: missing objectives, methodology, analysis, references, or measurable achievements. Faculty feedback is slow and inconsistent, and students usually learn what was missing only after losing marks or interview shortlists.

## Features

- **Document types:** Resume, Project report, Lab report, or a custom rubric you define.
- **Requirements check:** each expected section is marked Found, Partial (mentioned but no clear heading) or Missing.
- **Readiness score** out of 100 with a short verdict.
- **Structural suggestions:** section order, overly long paragraphs, missing numbers or citations, resume length, action verbs, passive voice and filler words.
- **Section balance:** words per section shown as bars, with warnings for thin sections.
- **Job description match** (Resume): top keywords from a job description, shown as matched or missing.
- **Progress tracker:** scores are saved in the browser's local storage so students can see improvement between checks.
- **Copy report:** copies the score, requirements and suggestions as plain text.

## Screenshots

| Resume | Project report | Lab report |
|---|---|---|
| ![Resume results](docs/screenshots/resume-results.png) | ![Project results](docs/screenshots/project-results.png) | ![Lab results](docs/screenshots/lab-results.png) |

## Run it

No build step or dependencies. Either:

1. Open `index.html` in any modern browser, or
2. Host it for free with GitHub Pages: repository **Settings > Pages > Deploy from a branch > main / root**.

## How to use

1. Choose a document type.
2. Paste the document text (or upload a `.txt` / `.md` file), or click **Load sample**.
3. For a resume, optionally paste a job description.
4. Click **Check document** and read the requirements, suggestions and score.
5. Fix the gaps, check again, and watch the score improve.

## How it works

1. The text is split into lines and short lines are treated as possible headings.
2. Each heading is matched against the checklist for the chosen document type (or your custom rubric) using keyword rules.
3. Sections found only in body text are marked Partial; sections not found are marked Missing.
4. Extra rules check order, length, numbers, citations, bullets, passive voice and filler words.
5. The score combines section coverage with the number of remaining issues.

## Tech

Plain HTML, CSS and JavaScript in a single file. No frameworks, no network requests.

## Limitations

- Matching is rule-based, so it works best on documents with plain section headings.
- Only pasted text and `.txt` / `.md` files are supported for now.

## Roadmap

- PDF and DOCX upload
- AI-generated suggestions with IBM watsonx
- Rubric template library for different subjects
- Teacher dashboard for class-level insights

## Project documents

- [Lean Canvas (PDF)](docs/FolioCheck_Lean_Canvas.pdf)
- [Presentation (PPTX)](docs/FolioCheck_Presentation.pptx)
- [Project screenshots (PDF)](docs/FolioCheck_Project_Screenshots.pdf)

## Author

Your Name | IBM SkillsBuild Masterclass 5

## License

MIT. See [LICENSE](LICENSE).
