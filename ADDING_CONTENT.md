# Adding Content to the GeoScape Lab Website

This is your one-page guide for everything you'll routinely add to the site.
**You don't need to know HTML.** You'll be copying ready-made blocks of code
and filling in blanks.

> Every place you add content has a clearly marked instructions block in the
> file itself. This document just tells you *which file* to open for *which task*.

---

## How to edit a file on github.com (works for everything below)

1. Open `https://github.com/geoscape-lab/geoscape-lab.github.io` in your browser
2. Click the file you want to edit
3. Click the **pencil icon** (top right of the file view) to start editing
4. Find the **TEMPLATE_START** / **TEMPLATE_END** block (look for the big
   bordered comment box)
5. **Copy** the block, **paste** it just under the comment, **replace** every
   `{{PLACEHOLDER}}` with your real value
6. Scroll down → **Commit changes** → wait 1 - 2 minutes → site is live

> Don't have your repo URL handy? It's:
> `github.com/geoscape-lab/geoscape-lab.github.io`

---

## Common tasks - quick reference

| What you want to do                 | File to open                          |
|-------------------------------------|---------------------------------------|
| Add a news item (card)              | `news.html`                           |
| Add a news detail page              | duplicate `pages/_TEMPLATE_news-detail.html` |
| Add a research publication          | `research.html`                       |
| Add a project                       | `projects.html`                       |
| Add a new lab member                | duplicate `pages/_TEMPLATE_member.html` AND edit `people.html` |
| Update someone's bio / photo / info | `pages/<lastname>.html`               |
| Add a publication to a profile      | `pages/<lastname>.html`               |
| Update the lab email or contact     | `contact.html`, `prospective.html`    |
| Update the home page hero text      | `index.html`                          |

---

## Detailed walkthroughs

### 1. Add a news item

This is **two steps** because each news item is a card on `news.html` plus
a full detail page.

**Step A — the card:**
- Open `news.html`, find the **HOW TO ADD A NEWS ITEM** comment near the top
- Copy the block between `TEMPLATE_START` / `TEMPLATE_END`
- Paste it just under the existing news cards
- Fill in `{{SLUG}}`, `{{DATE}}`, `{{TITLE}}`, `{{EXCERPT}}`

**Step B — the detail page:**
- Go to `pages/_TEMPLATE_news-detail.html`, copy its full contents
- Create a new file in `/pages` named `news-{{SLUG}}.html` (same slug as Step A)
- Paste the template, fill in placeholders, **delete the instruction comment block at the top**
- Commit

**Step C (optional) — image:**
- Upload an image to `/images` named `news-{{SLUG}}.jpg`
- If you skip this, the placeholder ◈ symbol shows automatically (still looks fine)

---

### 2. Add a research publication

- Open `research.html`
- Find the **HOW TO ADD A RESEARCH PUBLICATION** comment near the top
- Copy the `TEMPLATE_START` / `TEMPLATE_END` block, paste under the existing articles
- Fill in: `{{NUM}}`, `{{YEAR}}`, `{{JOURNAL}}`, `{{TITLE}}`, `{{AUTHORS}}`, `{{DOI_URL}}`
- Update the `{{NUM}}` numbers across all articles so they go 01, 02, 03, ... in order
- Commit

---

### 3. Add a project

- Open `projects.html`
- Find the **HOW TO ADD A PROJECT** comment
- If this is your first project, **delete** the `<p class="no-vacancies">There are no ongoing projects...</p>` line
- Copy the `TEMPLATE_START` / `TEMPLATE_END` block, paste inside `<div class="projects-grid">`
- Fill in `{{STATUS}}`, `{{TITLE}}`, `{{DESCRIPTION}}`
- Commit

---

### 4. Add a new lab member (3 - 4 minute job)

**Step A — create the profile page:**
- Open `pages/_TEMPLATE_member.html`, copy its full contents
- Create a new file at `/pages/{{LASTNAME}}.html` (lowercase last name, e.g. `kabir.html`)
- Paste the template, fill in **every** `{{PLACEHOLDER}}`
- Delete the instruction comment block at the top of the file
- Commit

**Step B — upload photo:**
- Upload to `/images` as `{{LASTNAME}}.jpg` (lowercase, exact match to the filename in Step A)
- If you skip this, the member's initials show in a circle instead

**Step C — add their card to the People page:**
- Open `people.html`, find the **HOW TO ADD A NEW MEMBER CARD** comment
- Copy the `TEMPLATE_START` / `TEMPLATE_END` block, paste inside the researchers grid
- Fill in `{{INITIALS}}`, `{{FIRST_LAST}}`, `{{ROLE}}`, `{{ONE_LINER}}`, `{{LASTNAME}}`
- Commit

That's it. New member is live.

---

### 5. Update an existing member's profile

- Open `pages/<lastname>.html` (e.g. `pages/shuvo.html`)
- Edit any text you want — biography paragraphs, research interests, education,
  publications. The structure is obvious; you can see how the existing items are
  formatted and follow the same pattern.
- For adding a publication, follow the **HOW TO ADD A PUBLICATION TO THIS PROFILE**
  comment that appears just below `<h2>Publications</h2>` in every profile.
- Commit

---

### 6. Replace someone's profile photo

- Make sure your new photo is **landscape or portrait JPG**, ideally 600x600
  pixels or larger, **named exactly `{{LASTNAME}}.jpg`** (e.g. `shuvo.jpg`)
- Upload to `/images`, replacing the existing file (GitHub will ask if you want
  to replace — say yes)
- That's it. The profile picks it up automatically.

---

## Things to remember

- **GitHub Pages is case-sensitive.** Photo filenames must match exactly. `Shuvo.jpg`
  ≠ `shuvo.jpg`. Always use lowercase.
- **Always delete the instruction comment block** when you create a new page from
  a `_TEMPLATE_` file. The comment is fine to keep on the templates themselves
  (they're for reference), but don't ship it on a real page.
- **Wait 1 - 3 minutes** after committing for changes to appear on the live site.
  If they don't appear, check the **Actions** tab on GitHub — every commit
  triggers a "pages build and deployment" workflow. A red ❌ there means the
  build failed and you'll need to look at the error message.
- **If something breaks the layout**, the easiest fix is the **History** tab on
  the file in github.com — find a previous commit that worked and click "Revert".

---

## When you need help

If you want to make a change that doesn't fit any of the templates above
(adding a whole new section, changing the colour scheme, adding a new page
type, fixing a layout bug), that's beyond copy-paste territory and you should
come back for help. Templates handle **content**; layout / styling / structure
changes are still HTML / CSS work.
