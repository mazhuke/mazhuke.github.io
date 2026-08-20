# Ke Zhu's Homepage

Personal academic website for **Ke Zhu**, built with [Academic Pages](https://academicpages.github.io/) (Jekyll) and hosted on GitHub Pages.

- **Live site:** https://mazhuke.github.io/
- **Repository:** https://github.com/mazhuke/mazhuke.github.io

You mainly edit **Markdown (`.md`) files**. After you push changes to GitHub, the website updates automatically (usually within a few minutes).

---

## Quick overview: which file to edit

| What you want to change | File to edit |
| --- | --- |
| About Me (homepage) | [`_pages/about.md`](_pages/about.md) |
| Publications / Research | [`_pages/research.md`](_pages/research.md) |
| Teaching / Courses | [`_pages/teaching.md`](_pages/teaching.md) |
| People (students) | [`_pages/people.md`](_pages/people.md) |
| Contact Info | [`_pages/contact.md`](_pages/contact.md) |
| Top menu links | [`_data/navigation.yml`](_data/navigation.yml) |
| Name, title, email, photo, Google Scholar, ORCID | [`_config.yml`](_config.yml) |
| Profile photo image file | [`images/`](images/) |

Do **not** edit files under `_site/` (if present). That folder is generated automatically.

---

## Markdown basics (enough for this site)

- A blank line separates paragraphs.
- A bullet list item starts with `- ` (dash + space).
- A numbered list item starts with `1. ` (one + period + space).
- A link looks like: `[visible text](https://example.com)`
- An email link looks like: `[name@example.com](mailto:name@example.com)`
- A section heading in this site often looks like:

```markdown
Section Title
======
```

- HTML comments (hidden on the website) look like:

```markdown
<!-- This text is hidden -->
```

---

## How to revise About Me

1. Open [`_pages/about.md`](_pages/about.md).
2. Edit the text under the top “front matter” block (the part between `---` lines at the top). Leave that top block alone unless you know what it does.
3. Common sections on this page:
   - Opening biography bullets
   - **Research Interests**
   - **Work Experience**
   - **Education**
   - **Awards**
   - **Service**
4. Save the file, then commit and push (see [Publish your changes](#publish-your-changes) below).

**Example:** add a new award

```markdown
Awards
======
- Fellow, International Statistical Institute, Since 2023
- Fellow, Journal of Econometrics, Since 2023
- Your New Award, Since 2026
```

---

## How to add a new publication

1. Open [`_pages/research.md`](_pages/research.md).
2. Find the correct section, for example:
   - `Machine learning in finance`
   - `Panel data analysis`
   - `Time series analysis`
   - `Others`
3. Add a **new line** under that section, using this format:

```markdown
1. Author, A., Author, B. and Zhu, K. (2026), Paper title. Journal Name. [PDF](https://...) [Journal Link](https://...) [Codes](https://...)
```

### Important rules for publications

- Always start the line with `1. ` (literally the number one).
- **Do not** manually renumber other papers.
- The website automatically numbers all papers continuously across all sections (1, 2, 3, …).
- Put the newest paper at the **top of its section** if you want newest-first ordering within that topic (follow the existing style).
- Only include links you actually have (`PDF`, `Journal Link`, `Codes`, `Conference Link`, etc.).
- You may omit links entirely if none are available.

**Example:** add one paper under Panel data analysis

```markdown
Panel data analysis
======
1. New, A. and New, B. (2026), A new panel paper title. In Submission. [PDF](https://example.com/paper.pdf)
1. New, A. and New, B. (2026), Second new paper title. In Submission. [PDF](https://...)
```

If you need a **new topic section**, copy an existing heading block:

```markdown
Your new topic
======
1. First paper in this topic...
```

---

## How to revise People

1. Open [`_pages/people.md`](_pages/people.md).
2. There are two sections:
   - **PhD Students** (current students)
   - **Graduated PhD Students**
3. To add a current student, add a bullet under **PhD Students**:

```markdown
- **Full Name**
```

4. To move someone to graduated status:
   - Delete their entry from **PhD Students**
   - Add their name under **Graduated PhD Students**

```markdown
Graduated PhD Students
======
- Former Student Name
```
---

## How to revise Teaching

1. Open [`_pages/teaching.md`](_pages/teaching.md).
2. Each course is one bullet line:

```markdown
- XXXX (Spring 2022, 2023, 2024, 2025)
```

3. To add a course, copy a line and edit the code, title, and semesters/years.
4. To update years (for example after teaching again), edit only the year list in parentheses.

---

## How to revise Contact Info

1. Open [`_pages/contact.md`](_pages/contact.md).
2. Update email and/or phone:

```markdown
**Email:** name@example.com

**Phone:** (000) 0000-0000
```

3. If you also want the sidebar email updated, change `email` under `author:` in [`_config.yml`](_config.yml) as well.

---

## How to update the sidebar profile (name, title, photo, links)

Edit [`_config.yml`](_config.yml), in the `author:` section near the top.

Common fields:

```yaml
author:
  name             : "Your Name"
  avatar           : "profile.png"
  bio              : "Your Title"
  employer         : "Your University"
  email            : "name@example.com"
  googlescholar    : "https://scholar.google.com/citations?user=XXXXXXXX"
  orcid            : "https://orcid.org/ACCT-0000-0000-0000"
```

### Change the profile photo

1. Put the image file in the [`images/`](images/) folder (for example `images/profile.png`).
2. Set `avatar` in `_config.yml` to that filename only (not a full path):

```yaml
avatar: "profile.png"
```

3. Prefer a square photo. PNG or JPG is fine.

---

## How to change the top navigation menu

Edit [`_data/navigation.yml`](_data/navigation.yml):

```yaml
main:
  - title: "Research"
    url: /research/
  - title: "Teaching"
    url: /teaching/
  - title: "People"
    url: /people/
  - title: "Contact"
    url: /contact/
```

- `title` is the text shown in the menu.
- `url` must match the page `permalink` (for example `/people/`).

---

## Publish your changes

### edit directly on GitHub

1. Open the repository: https://github.com/mazhuke/mazhuke.github.io
2. Open the file you want (for example `_pages/research.md`).
3. Click the pencil icon to edit.
4. Save with **Commit changes**.

Then wait a few minutes and refresh https://mazhuke.github.io/.

---

## Troubleshooting

| Problem | What to check |
| --- | --- |
| Site does not update | Wait 2–5 minutes; hard-refresh the browser; check the repo **Actions** / Pages settings |
| Publication numbers look wrong | Make sure each paper line starts with `1. ` and is under a section heading |
| Photo missing | Confirm the file exists in `images/` and `author.avatar` matches the filename exactly |
| Broken link | Check that the URL is complete and wrapped as `[text](https://...)` |
| Accidental site breakage | Restore the previous commit on GitHub, or ask someone to revert the last change |

## File map (for maintainers)

```text
_config.yml          Site-wide settings and sidebar profile
_data/navigation.yml Top menu
_pages/about.md      Homepage / About Me
_pages/research.md   Publications
_pages/teaching.md   Courses
_pages/people.md     Students
_pages/contact.md    Contact information
images/              Profile photo and other images
```
