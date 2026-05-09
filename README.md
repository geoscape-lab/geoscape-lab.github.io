# GeoScape Lab — Website

Official website for **GeoScape Lab**, an independent research collective working on Disaster Risk Assessment, Water & Land Dynamics, Environmental Economics, and Climate Change Adaptation.

**Live site:** [https://geoscape-lab.github.io](https://geoscape-lab.github.io)
**Repository:** [github.com/geoscape-lab/geoscape-lab.github.io](https://github.com/geoscape-lab/geoscape-lab.github.io)
**Contact:** geoscape.lab@gmail.com

---

## Editing the website

For routine updates (adding a news item, a publication, a project, a new member, or updating an existing profile), see **[ADDING_CONTENT.md](ADDING_CONTENT.md)** — a step-by-step guide that requires no coding knowledge.

Every editable section in the site has a clearly marked instructions block built into the HTML, so you'll always have the templates right where you need them.

---

## File Structure

```
geoscape-lab.github.io/
├── index.html              ← Home page
├── about.html              ← About GeoScape Lab
├── people.html             ← All members
├── research.html           ← Published articles
├── projects.html           ← Ongoing projects
├── news.html               ← News & updates
├── prospective.html        ← Join Us / prospective researchers
├── contact.html            ← Contact page
├── ADDING_CONTENT.md       ← Cheat sheet for editors
├── README.md               ← This file
├── css/
│   └── style.css           ← All styles
├── js/
│   └── main.js             ← Navigation script
├── images/                 ← Profile photos and hero image
└── pages/
    ├── shuvo.html          ← Ragib Mahmood Shuvo (Co-Director)
    ├── dola.html           ← Sumaia Kashem (Co-Director)
    ├── ghosh.html          ← Prem Kumer Ghosh
    ├── hasan.html          ← Md. Zahid Hasan
    ├── chowdhury.html      ← Radwan Rahman Chowdhury
    ├── bhuiyan.html        ← Manoshi Bhuiyan
    ├── ruponti.html        ← Farhana Rabbi Ruponti
    ├── news-lab-founded.html       ← News article (lab founding)
    ├── _TEMPLATE_member.html       ← Skeleton for new member pages
    └── _TEMPLATE_news-detail.html  ← Skeleton for new news articles
```

---

## How updates work (technical notes)

The site is a static HTML / CSS / JS site served by GitHub Pages. Every push to the `main` branch triggers an automatic redeploy, which usually completes within 1–2 minutes.

**To make a change:**
1. Edit the relevant file on github.com (click the file → pencil icon → edit → Commit changes), or via Git on your local machine.
2. Wait 1–2 minutes for GitHub Pages to rebuild.
3. Refresh the live site (hard refresh with Ctrl+Shift+R / Cmd+Shift+R if you don't see the change).

**If a deploy fails:** check the **Actions** tab of the repository for the "pages build and deployment" workflow. A red ❌ tells you the build broke; click into it for the error message.

---

## Fonts

The site uses **EB Garamond** (serif, for headings) and **DM Sans** (sans-serif, for body) loaded from Google Fonts. An internet connection is required to display them correctly.

---

## Beyond simple edits

Routine content updates are designed to be self-service via the templates. For changes that go beyond content — restructuring the navigation, changing colours or fonts, adding a brand-new page type, or fixing layout bugs — those are HTML / CSS work and need a developer.
