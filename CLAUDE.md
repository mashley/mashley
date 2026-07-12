# CLAUDE.md — mashley.com

Personal consultant landing page for **Michael "Mash" Ashley** ("Consultant for
New Founders"). Static site, no framework, no build step.

> Note: this repo was originally used to run a beginner web-dev workshop. That
> teaching material now lives in `workshop-guide.md` (a shareable handout) and no
> longer governs work in this repo. Treat the owner as an experienced developer.

## Structure

- `index.html` — the entire site: HTML plus all CSS inlined in a single `<style>`
  block in the `<head>`. There is no separate stylesheet and no JS.
- `images/` — `michael.jpg` (headshot), `working-session.jpg`.
- `README.md` — GitHub profile blurb (kept separate from the site content).
- `workshop-guide.md` — the beginner-workshop handout; unrelated to the live site.

## Conventions

- **One file.** Keep everything in `index.html` with inline CSS unless there's a
  real reason to split. This is intentionally a simple, dependency-free page.
- **Palette lives in CSS variables** at the top of the `<style>` block
  (`--orange`, `--orange-dark`, `--lime`, `--ink`, `--muted`, `--cream`,
  `--white`). Change colors there, not inline.
- **Layout**: content is centered in a `.wrap` container (max-width ~820px).
  Sections alternate white and `--cream` backgrounds; cream sections use rounded
  corners.
- **Comments**: the file uses plain-English section comments (a habit from its
  workshop origins) — keep new sections readable and lightly commented in the
  same style.
- Preview by opening `index.html` directly in a browser — no server needed.

## Deploy

- Remote: `github.com/mashley/mashley`, default branch `main`.
- Ship changes by committing and pushing to `main` (the `/deploy` skill handles
  the pre-flight checks, but for a static page a plain commit + push is fine).
- Only commit or push when explicitly asked.
