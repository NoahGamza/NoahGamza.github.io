# Noah Gamza — Portfolio (GitHub Pages, no framework)

One file: `index.html`. No build step, no Quarto, no Jekyll — write HTML, push, it's live.

## What's in here

- `index.html` — the whole site. Plain HTML + inline CSS, styled after the flat
  tool-list look of [Baseball Hopper](https://willybeanes.github.io/).
- `assets/` — put `resume.pdf` here (referenced by the "Resume" link).

Search the file for `TODO` — every placeholder link (LinkedIn, GitHub, Substack,
the Hamptons League Scout app URL, the BDR write-up, Substack posts) is marked.

## 1. Preview it locally

No server needed — just open the file directly in a browser:

```bash
open index.html        # macOS
# or just double-click index.html in Finder
```

## 2. Put it on GitHub

Pick one of two setups:

**Option A — this becomes your main site** (`https://yourusername.github.io`):
create a new GitHub repo named *exactly* `yourusername.github.io` (replace with your
real GitHub username). Anything in that repo's root is served at that URL
automatically — GitHub turns Pages on for you the moment the repo exists with that
name.

**Option B — a project site** (`https://yourusername.github.io/repo-name/`):
name the repo anything you want, then turn Pages on manually: repo → **Settings** →
**Pages** → under "Build and deployment," set **Source** to "Deploy from a branch,"
branch `main`, folder `/ (root)` → **Save**.

Either way, the push itself is the same:

```bash
# from this folder
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

Give it a minute after the first push — GitHub needs to build and deploy it. Your
URL will be live at whichever address matches the option you picked above.

## 3. Updating later

Edit `index.html`, then:

```bash
git add index.html
git commit -m "Add new project"
git push
```

It redeploys automatically within a minute or two. No publish command, no render
step — that's the whole tradeoff versus the Quarto version: less structure and
theming, but there's genuinely nothing to break.

## Adding a new project

Copy one `<li>...</li>` block under the right `<ul class="tools">` section
(Baseball or Basketball), change the link, title, and one-line description. That's
the entire workflow for keeping this current.
