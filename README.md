# Thanh Hiep Vo — Portfolio

Academic-style personal website at [thanhhiepvo.github.io](https://thanhhiepvo.github.io), built with [Jekyll](https://jekyllrb.com/) using a layout inspired by [Quang Truong](https://quang-truong.github.io/) and [Martin Saveski](https://faculty.washington.edu/msaveski/).

## Site structure

```
.
├── _config.yml           # Site settings
├── _data/                # Content (edit these to update the site)
│   ├── main_info.yaml    # Name, title, email, social links, navbar
│   ├── experience.yaml   # CV timeline entries
│   └── publications.yaml # Research / thesis entries
├── _projects/            # One markdown file per project → its own page
├── _includes/            # Reusable partials
│   ├── head.html         # <head>: meta tags, CSS, JS
│   ├── header.html       # Photo, name, title, social links
│   ├── navbar.html       # Nav (rendered from main_info.yaml `nav`)
│   ├── social-links.html # Shared icon row (header + footer)
│   └── footer.html
├── _layouts/
│   ├── default.html      # Page shell
│   └── project.html      # Individual project page
├── index.html            # Main page sections
├── libs/                 # CSS, JS, fonts (Skeleton, Font Awesome, etc.)
└── assets/profile-pics/  # Profile photo
```

## Updating content

Edit the YAML files in `_data/` — no need to touch HTML for most updates:

| File | What to change |
|------|----------------|
| `main_info.yaml` | Name, title, email, social links, navbar items |
| `experience.yaml` | Work and education timeline (CV section) |
| `publications.yaml` | Research and thesis entries |

For news, bio text, or skills, edit `index.html` directly.

### Social links

Set a URL in `main_info.yaml` to show that icon; leave it as `""` to hide it.
Supported keys: `github`, `huggingface`, `linkedin`, `scholar`.

### Adding a project

Create a new file in `_projects/`, e.g. `_projects/my-project.md`:

```markdown
---
layout: project
title: "My Project"
subtitle: "One-line description"
selected: "y"      # "y" shows it under the Projects → Selected tab
order: 10          # controls ordering on the homepage
github: ""         # optional — set a URL to show a "Code" button
---

Markdown body goes here.
```

It appears on the homepage automatically and gets its own page at
`/projects/my-project/`. No HTML edits needed.

## Resume (private)

`Resume.pdf` is in `.gitignore` and is **not** published. The CV section shows a timeline only, with “available on request.”

## Local preview

macOS ships with an old Ruby (2.6) that cannot run Jekyll. Use **Homebrew Ruby** instead.

### One-time setup

```bash
# Install Ruby (skip if already installed)
brew install ruby

# Add Homebrew Ruby to your PATH (add this line to ~/.zshrc)
export PATH="/opt/homebrew/opt/ruby/bin:/opt/homebrew/lib/ruby/gems/4.0.0/bin:$PATH"

# Reload shell
source ~/.zshrc

# Install dependencies
cd /Users/thanhhiepvos/Code/thanhhiepvo.github.io
bundle install
```

### Run locally

```bash
cd /Users/thanhhiepvos/Code/thanhhiepvo.github.io
bundle exec jekyll serve
```

Open **http://localhost:4000** in your browser.

Jekyll watches for file changes and rebuilds automatically. Press `Ctrl+C` to stop the server.

To build without serving (output goes to `_site/`):

```bash
bundle exec jekyll build
```

## Deploy

Push to the `general` branch. GitHub Pages builds automatically.

**Settings → Pages → Source:** `general` branch, `/ (root)`.

## Acknowledgement

Layout based on [Martin Saveski's website template](https://github.com/msaveski/www_personal) and [quang-truong.github.io](https://github.com/quang-truong/quang-truong.github.io).
