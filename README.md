# resume — A Compact, Full-Width LaTeX Resume Template

A clean, single-column LaTeX resume template for industry job
applications. Every section (summary, skills, experience, education)
spans the full text width, with dates and locations aligned to the
right edge of the same line — no wasted margins, no mismatched
columns. Designed to fit comfortably on one page.

**GitHub:** https://github.com/tahahb79/Resume-Template-with-LaTeX


> **Looking for a longer academic CV format instead** (with
> publications, research projects, and references)? See the
> companion [CV template](https://github.com/tahahb79/Full-Width-Academic-Industry-CV-Resume-Template)  — it uses the same `resume.cls` file.

## Files

| File                   | Purpose                                                        |
|------------------------|------------------------------------------------------------------|
| `resume-template.tex`  | Placeholder resume showing every command in use — copy this and fill in your own details |
| `resume.cls`           | The class defining fonts, colors, and layout commands            |

`resume.cls` must stay in the same folder as your `.tex` file.

> **Note:** `resume-template.tex` uses placeholder data on purpose.
> Keep your own filled-in resume (with your real contact details) in
> a private location if you'd rather not publish it.

## Usage

### On Overleaf
1. Create a new blank project.
2. Upload `resume-template.tex` (rename it to `resume.tex` or
   whatever you like) and `resume.cls` into the project root (same
   folder).
3. Set your `.tex` file as the main file (Overleaf usually detects
   this automatically; if not, right-click it in the file list and
   choose **Set as Main File**).
4. Compile with **pdfLaTeX**.

### Locally
```bash
pdflatex resume.tex
```
Requires a standard TeX Live / MiKTeX installation with the
`fontawesome`, `fancyhdr`, `hyperref`, `xcolor`, `etoolbox`,
`palatino`, and `lastpage` packages (all included in most TeX
distributions by default).

## Available Commands

| Command | Description |
|---|---|
| `\name{...}` | Your name, centered at the top |
| `\personalinfo{city}{country}{postcode}{email}{phone}` | Contact line under your name |
| `\cvsection{Title}` | A section heading with an underline rule |
| `\cveventfull{date}{title}{organization}{location}` | An entry with a date/org header (education, jobs) |
| `\cvitemfull{text}` | A full-width bullet point |
| `\cvsubitemfull{text}` | An indented sub-bullet, still full width |

## Customization

- **Font size**: this template sets a slightly smaller `10.5pt` size
  locally (see the top of the `.tex` file) to help fit on one page,
  without changing the shared `resume.cls`.
- **Margins**: adjust the `geometry` package options in the `.tex`
  file (currently `1.5cm`).
- **Spacing between entries**: controlled by `\smallskipamount` and
  `\medskipamount`, set near the top of the `.tex` file.
- **Accent color**: change the `accentblue` color definition near the
  top of `resume.cls`.

## License

This project is licensed under the [MIT License](LICENSE).

Copyright (c) 2026 Ali Habibi
