# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) and other AI assistants when working in this repository.

## Repository purpose

This is **`sukhvirk76/sukhvirk76`** — a GitHub **special / "magic" profile repository**. Because the repository name is identical to the account name, GitHub treats its root `README.md` as the owner's **profile README**: whatever is in `README.md` renders directly on the public profile page at https://github.com/sukhvirk76.

This is *not* a software project. There is no application, build system, package manager, test suite, or deployable artifact. The "product" is the rendered profile page. Treat content and presentation — not code — as the deliverable.

## Current state

As of this file's creation, the repository is **empty**: it contains no commits other than the ones introducing this documentation, and there is no `README.md` yet. Creating a `README.md` is the natural next step to make the profile page show something.

> When this changes, update this file. If real source code is ever added, replace the sections below with an accurate description of the actual structure, build, and test commands.

## Conventions

### README / profile content
- The profile README lives at `/README.md` (repository root). It must be there and named exactly `README.md` for GitHub to render it on the profile.
- Markdown is GitHub-Flavored Markdown (GFM). HTML is permitted for layout (centering, image sizing, badge rows), but a limited subset — GitHub sanitizes `<script>`, inline event handlers, and most CSS.
- Prefer accessible content: provide `alt` text for images and meaningful link text.
- Keep secrets and personal contact details out of the README — it is fully public.

### Commits
- Use clear, descriptive commit messages in the imperative mood (e.g. "Add profile README", "Update tech stack badges").
- This is a personal repo; keep history clean and readable.

### Branching & workflow
- Default development happens on the branch assigned for the current task. Do **not** push to `main`/`master` (or any other branch) without explicit permission.
- Push with `git push -u origin <branch-name>`.
- Do **not** open a pull request unless explicitly asked.

## Working notes for AI assistants

- Because there is no code, there are no lint/test/build steps to run or verify. Validate Markdown by rendering/preview reasoning rather than executing tooling.
- If asked to "build out the profile," typical additions include: an intro/bio, current focus, tech stack badges (e.g. shields.io), social links, and GitHub stats widgets. Confirm the desired tone (professional vs. playful) and which links/handles to include before adding personal data.
- If the user later turns this into an actual code project, re-run repository analysis and rewrite this CLAUDE.md to document the real architecture, commands, and conventions.
