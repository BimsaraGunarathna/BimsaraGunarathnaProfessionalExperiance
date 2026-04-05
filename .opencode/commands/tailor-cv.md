---
description: Create a tailored CV from a job description
---

You are a CV tailoring expert. Create a targeted CV for Bimsara Gunarathna from a job description.

## Input

$ARGUMENTS — job description (text or URL). Fetch URL if provided.

## Source Materials

1. @BimsaraGunarathna-SoftwareEngineer.md — Base CV
2. @bimsara_career_report.md — Career report with projects, metrics, timeline
3. @bimsara_gunarathna_contributions.md — Contributions data

## Process

### Step 1: Analyze Job Description
- Extract company, role, requirements, preferred skills, seniority, industry
- Identify top 5–7 ATS keywords
- Determine hiring manager priorities

### Step 2: Draft CV (in memory — no files yet)
- Rewrite Professional Summary targeting the role's requirements
- Reorder/rephrase bullets to highlight relevant achievements
- Mirror JD terminology exactly (e.g., "CI/CD pipelines" if they say it)
- Prioritize Skills section to match role demands
- Only rephrase and reorder — never fabricate

### Step 3: Present for Review
Output the **full CV** in the terminal. Then summarize:
- What was emphasized/de-emphasized and why
- ATS keywords targeted
- Gaps between JD and Bimsara's experience

Iterate based on feedback — show the updated CV each round.

### Step 4: Approval & PDF Generation
Ask: **"The CV looks good? Shall I generate the PDF?"** — do NOT write files until confirmed.

After approval:
1. Create `application/` directory if needed
2. Write CSS to `application/cv-style.css` (see CSS template below)
3. Write CV to `application/bimsara-{company}-{role}.md` with front-matter referencing the CSS file by **absolute path**
4. Run: `npx --cache "$TMPDIR/npm-cache" md-to-pdf <absolute-path-to-md-file>`
5. Verify PDF, check page count, report path
6. If >1 page, trim content and/or tighten CSS, then regenerate until it fits on exactly 1 page
7. If content fits but leaves excessive blank space at the bottom, increase font size/spacing or restore cut bullets to fill the page

## Formatting Rules (all mandatory)

### ATS Content Rules
- **Section order:** Contact Info → Professional Summary → Skills → Experience → Certifications → Education
- **Left-aligned, plain text only** — no tables, columns, icons, graphics, or horizontal rules
- **Dates:** plain text, hyphens not en-dashes (e.g., `November 2023 - Present`)
- **Acronyms:** expand on first use (e.g., "Amazon Web Services (AWS)")
- **Section title:** "Skills" not "Technical Skills"
- **Standard capitalization** — no ALL CAPS or all lowercase
- **Action verbs + metrics** — quantify achievements where data exists
- **No internal references** — no Jira IDs, internal version numbers, or internal tool names. Use generic descriptions (e.g., "100+ pull requests" not "112 Jira issues")

### PDF Typography
- **Font:** Calibri or Arial; max 2 families
- **Sizes:** Name 18–20pt bold | Headings 12–14pt bold | Job titles 10.5–11pt bold | Body 10–11pt (10.5pt ideal, never <10pt)
- **Margins:** 10–12.7mm (use 10mm for tight fit; never <10mm)
- **Line spacing:** 1.05–1.15 body | 1–2pt between bullets | 6–8pt around headings
- **PDF must fit on exactly 1 page.** Be ruthless — only the most impactful, role-relevant bullets. If it overflows, cut weaker points or tighten wording until it fits

### md-to-pdf Known Issues
- **Never use inline CSS in the YAML `stylesheet` array** — md-to-pdf treats it as a filename, causing `ENAMETOOLONG`. Always use an external `.css` file.
- **Stylesheet paths must be absolute** — relative paths fail with `ENOENT` because md-to-pdf doesn't resolve relative to the markdown file.
- **Use `npx --cache "$TMPDIR/npm-cache" md-to-pdf`** — the global npm cache may have permission issues. Using a temp cache avoids this.
- **Always pass the absolute path to the .md file** when running md-to-pdf.
- **pandoc/weasyprint/pdflatex are not available** on this system. md-to-pdf (Puppeteer/Chromium) is the only working PDF engine.
- **1-page fitting is iterative** — the built-in PDF reader may show fewer pages than the actual PDF. Always have the user verify page count and adjust CSS/content accordingly.

### CSS File Template (`application/cv-style.css`)
```css
body { font-family: Calibri, Arial, sans-serif; font-size: 10.5pt; line-height: 1.15; color: #333; margin: 0; padding: 0; }
h1 { font-size: 20pt; margin: 0 0 2pt 0; color: #000; }
h2 { font-size: 12pt; margin: 8pt 0 3pt 0; border-bottom: 1px solid #ccc; padding-bottom: 1pt; color: #000; }
h3 { font-size: 10.5pt; margin: 4pt 0 1pt 0; color: #000; }
h4 { font-size: 10.5pt; margin: 3pt 0 1pt 0; color: #000; }
p { margin: 2pt 0; }
ul { margin: 1pt 0; padding-left: 14pt; }
li { margin: 1pt 0; }
em { font-size: 9.5pt; }
a { color: #0563C1; text-decoration: none; }
```

### Front-matter Template
```yaml
---
pdf_options:
  format: A4
  margin: 12.7mm
stylesheet:
  - /absolute/path/to/application/cv-style.css
---
```
