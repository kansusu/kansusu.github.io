# Yifan Zhu — personal site

Plain HTML + CSS. No build step. GitHub Pages serves it as-is.

## File layout

```
site/
├── index.html          Home (profile, bio, news, contact)
├── research.html       Research themes
├── publications.html   Publications by topic
├── service.html        Reviewer service
├── style.css           Shared styles
├── assets/
│   ├── profile.jpg     Your headshot (drop here)
│   └── cv.pdf          Compiled CV (drop here)
└── README.md
```

## Deploy to GitHub Pages

Two options. Pick one.

### Option A — user site (recommended)
Hosted at `https://<username>.github.io`.

```bash
# from the parent folder
cd /Users/yifanzhu/Downloads/internship/site
git init
git add .
git commit -m "Initial personal site"
gh repo create <username>.github.io --public --source=. --remote=origin --push
# In GitHub repo settings → Pages → Source: "Deploy from branch", main, /(root)
```

Wait 1–2 minutes, then your site is at `https://<username>.github.io`.

### Option B — project site
Hosted at `https://<username>.github.io/<repo>`.

Same as above but name the repo anything (e.g. `personal-site`). All internal
links are relative, so it works either way.

## Things to fill in before going live

- [ ] `assets/profile.jpg` — drop your headshot here (square, ~400×400 minimum)
- [ ] `assets/cv.pdf` — compile `Yifan_Zhu_Resume.tex` and drop the PDF here
- [ ] `index.html` — update the GitHub link (`https://github.com/<username>`)
- [ ] `publications.html` — fill in real PDF/arXiv/code links for each `[#]` placeholder
- [ ] `index.html` — verify all news dates are accurate
- [ ] `service.html` — confirm CV4Edu and LREC 2026 URLs

## Editing notes

- Bio paragraph on the home page is the first thing recruiters read. Keep it 3–5 sentences.
- News list: keep ~6 most recent. Older items drift off naturally.
- Publications: bold your own name with `<span class="pub-self">Yifan Zhu</span>`.
- All section anchors on the publications page (`#fpo`, `#cgt`, `#multimodal`, `#umr`) are linked from the research page — don't rename them without updating both.

## Local preview

```bash
cd /Users/yifanzhu/Downloads/internship/site
python3 -m http.server 8000
# open http://localhost:8000
```
