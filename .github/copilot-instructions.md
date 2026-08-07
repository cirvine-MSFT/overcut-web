# Copilot instructions — Overcut website

**Read [`../AGENTS.md`](../AGENTS.md) first.** It is short and it is the working
agreement.

This repository is the website for Overcut™ and nothing else. The game lives in a
separate private repository. Do not attempt to reason about game code from here.

## The most important thing

**This repository is public. The game repository is not.** Anything committed
here is immediately visible to anyone, including on branches, and making a
repository private later does not un-publish what has already been seen. Treat
every commit as permanent publication.

That is fine for site code, which is HTML, CSS, and build configuration. It is
not fine for reveal material. Do not commit concept art, launch dates, trailers,
or unannounced feature copy until they are meant to be public.

## Stack

| Piece | Choice | Notes |
|---|---|---|
| Framework | Astro, static output | No server runtime is needed before M5 |
| Language | TypeScript | Strict |
| Styles | Tailwind CSS | |
| Lint + format | Biome | One tool, replaces ESLint and Prettier |
| Runtime | Node 22 LTS, pnpm | |
| Hosting | Azure Static Web Apps, free tier | |

Do not add a framework, a UI library, or a CMS without asking. The site is
deliberately small. It will get a backend at M5 — a leaderboard — and that
backend will be a **separate, private repository** orchestrated with .NET Aspire,
not an API route in this one.

## Writing copy

The game's authoritative description is in the private repository's `GAME.md`.
Never invent details about how Overcut plays. The constraints that matter most:
it is collisionless, all cars perform identically, abilities never hinder a
rival, and it is played only from inside the car. The ability system's specifics
are genuinely undecided — do not write copy that implies otherwise.

Use `Overcut™` on first prominent use on a page.

## Images

**No car imagery until the bespoke car exists.** The vehicle currently in the
game is Epic's Unreal Engine template placeholder, is scheduled for deletion, and
is not ours to present as Overcut.

Prefer SVG for UI and diagrams. Raster images should be WebP or AVIF, sized for
the layout, and must carry meaningful `alt` text.

## Accessibility and performance

These are requirements, not aspirations:

- Semantic HTML. Headings in order. Landmarks present.
- Text contrast at WCAG AA or better.
- Every interactive element reachable and operable by keyboard, with a visible
  focus style.
- Respect `prefers-reduced-motion`.
- Ship as little JavaScript as possible — Astro's default is zero, so adding any
  should be a decision rather than an accident.

## Conventions

- Components in `src/components/`, pages in `src/pages/`, layouts in
  `src/layouts/`, static files in `public/`.
- PascalCase for component files (`SiteHeader.astro`), kebab-case for routes.
- Design tokens in one place. No hard-coded hex values in components.
- Never commit secrets. The Static Web Apps deployment token is a GitHub Actions
  secret and must not appear in the repository or in a workflow file as a literal.
