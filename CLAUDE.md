# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) and other AI assistants when working in this repository.

## Repository purpose

This is **`sukhvirk76/sukhvirk76`** — a GitHub **special / "magic" profile repository**. Because the repository name is identical to the account name, GitHub renders its root `README.md` as the owner's **profile README**: whatever is in `README.md` appears on the public profile page at https://github.com/sukhvirk76.

This is *not* a software application. There is no build system, package manager, or runtime. The "product" is the rendered profile page. Treat content, presentation, and the supporting automation — not application code — as the deliverable.

## Structure

```
.
├── README.md                       # The profile page (rendered on github.com/sukhvirk76)
├── CLAUDE.md                       # This file
├── .gitignore
└── .github/
    └── workflows/
        └── snake.yml               # Generates the contribution-graph "snake" SVG
```

### `README.md`
The profile content. Built with GitHub-Flavored Markdown plus a small amount of HTML for layout (centering, badge rows, image sizing). Sections: intro, about, tech badges, GitHub stats widgets, contribution snake, and connect links. Most personal details are intentionally generic placeholders marked with inline notes — they are meant to be customized.

External widgets used (all render as plain `<img>` tags, no code to run):
- **shields.io** — static tech/skill badges.
- **github-readme-stats** (`github-readme-stats.vercel.app`) — stats + top-languages cards.
- **streak-stats** (`streak-stats.demolab.com`) — contribution streak card.
- **komarev ghpvc** — profile view counter.

### `.github/workflows/snake.yml`
A GitHub Actions workflow that runs daily (and on pushes to `main`) to generate the animated contribution-graph snake via `Platane/snk`, then publishes the SVG to a dedicated `output` branch using `crazy-max/ghaction-github-pages`. `README.md` references the SVG at the raw URL on the `output` branch. The workflow needs `contents: write` permission (already declared in the file) and the default `GITHUB_TOKEN`.

## Conventions

### README / profile content
- The profile README must live at `/README.md` (repository root), named exactly `README.md`, for GitHub to render it on the profile.
- Use GFM; HTML is allowed but GitHub sanitizes `<script>`, inline event handlers, and most CSS. Stick to the safe subset (alignment, `<img>`, `<a>`, `<sub>`, `<details>`).
- Provide `alt` text for images and meaningful link text (accessibility).
- Keep secrets and private contact info out of the README — it is fully public.
- Username `sukhvirk76` is hard-coded into widget URLs; if the account name ever changes, update every widget URL and the snake raw URL.

### Commits
- Clear, descriptive messages in the imperative mood (e.g. "Add profile README", "Update tech stack badges").

### Branching & workflow
- Develop on the branch assigned for the current task. Do **not** push to `main`/`master` without explicit permission.
- Push with `git push -u origin <branch-name>`.
- Do **not** open a pull request unless explicitly asked.
- Note: the `output` branch is **machine-generated** by `snake.yml` — never hand-edit or commit to it manually.

## Working notes for AI assistants

- There is no code, so there are no lint/test/build commands to run. "Validation" means checking Markdown/HTML renders correctly and that widget URLs reference the right username.
- The snake animation only appears once the `snake.yml` workflow has run successfully at least once (it creates the `output` branch). Until then its `<img>` will be broken — this is expected on a fresh repo.
- When asked to personalize, confirm tone (professional vs. playful) and which real links/handles to include before adding personal data; replace the placeholder text and commented-out social links in `README.md`.
- If this repo is ever turned into a real code project, re-analyze and rewrite this file to document the actual architecture, commands, and conventions.
