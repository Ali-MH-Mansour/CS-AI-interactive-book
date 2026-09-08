# Interactive Book — Fundamentals of CS & AI / الكتاب التفاعلي

> The interactive, animated version of the course, adopted at **RE03=a** (Message 014):
> a bilingual (EN ⇄ العربية) book where every idea that *can* be modelled becomes a
> **play / step / replay** animation, each with a short **commentary on what to notice**
> (the User's «الشرح مع الحركات مع شرحها وتعليق عليها»).

## What is here / ما الموجود

| File | Purpose |
|------|---------|
| `index.html` | Book **cover + table of contents** (9 lectures, 4 modules). Language toggle top-right; choice remembered across pages. |
| `lecture-01.html` | **Lecture 1 — Information & Data Representation.** The first fully interactive chapter and the working **template** for the rest. Four animations: §1 the bit / information content, §2 decimal→binary, §3.3 two's complement, §5.3 UTF-8 encoding — each followed by a "💡 What to notice / ما الذي نلاحظه" commentary box. |

Each page is **self-contained**: no build step, no internet, no dependencies. Open the file in any
browser, or drop the folder onto a web host as-is.

## Two versions of every lecture / نسختان لكل محاضرة

- **Interactive** (this folder) — animations for the "process" examples, for exploring on screen / in class.
- **Text reference** — the existing per-lecture handouts `../lecture-0N-en.md` / `../lecture-0N-ar.md`
  (and their PDFs) carry the *same wording* with no animation: the printable / revision copy.

## Publishing to GitHub Pages / النشر على GitHub Pages

The book is plain static HTML, so GitHub Pages serves it directly — **no Actions build required**
for this standalone form. Once the User creates/nominates the target repo (see the activity's
User Task) and approves the push:

1. `git init` in this folder (or add it to the nominated repo), commit `index.html` + the `lecture-*.html` files.
2. Push to GitHub.
3. Repo **Settings → Pages → Source = Deploy from a branch**, branch `main`, folder `/ (root)`.
4. The book is live at `https://<user>.github.io/<repo>/` — `index.html` is the cover.

> **Relation to the Quarto architecture (RE03=a).** RE03 adopted "Quarto Book → GitHub Pages" so
> one source can emit both the interactive site and a text/PDF per lecture. These self-contained
> HTML chapters are exactly the **animation widgets** that Quarto embeds — building them first
> means they are publishable *now* and drop into the `../cs-ai-quarto/` scaffold later without
> rework. Whether to (a) keep the book as standalone HTML pages or (b) wire the widgets into the
> Quarto book for single-source PDF is an implementation choice to revisit as chapters accumulate;
> the text/PDF references already exist as the `lecture-*.md` handouts either way.

## Roadmap / خارطة الطريق

- [x] L1 — Information & Data Representation (interactive)
- [x] L2 — Computer Architecture (interactive) · [ ] L3 — Algorithmization · [ ] L4 — Software Life Cycle
- [ ] L5 — Information Security · [ ] L6 — Computer Networks
- [ ] L7 — Intro to AI · [ ] L8 — Mathematics of ML · [ ] L9 — AI in Practice

Chapters 2–9 already exist as text handouts (EN + AR) and are converted to interactive chapters
one per run, reusing `lecture-01.html` as the template.
