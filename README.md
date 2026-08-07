# Overcut — website

The website for **Overcut**™, a serious, collisionless competitive circuit racer
where precise driving wins races and strategy determines who can sustain it.

- **Live site:** <https://overcut.racing>
- **Development writing:** <https://caseyirvine.dev>

This repository contains **only the website**. The game itself lives in a
separate, private repository, and the reasoning for that split is recorded in the
game repo as `docs/decisions/0035-the-website-is-not-in-this-repository.md`. The
short version: the game repository is private and cannot currently be published,
its binary assets are Git LFS–tracked and metered, and its merge gate compiles
Unreal Engine — none of which a static site should inherit.

## What this site is, and is not

It is a **product site**. It exists to say what Overcut is and, later, to let
people play it and compare lap times.

It is **not** a devlog. Development writing goes to `caseyirvine.dev`.

## Status

Pre-launch. The site is a placeholder until concept art exists.

There is deliberately **no car imagery yet**. The only vehicle currently in the
game is Epic's placeholder from the Unreal Engine templates; it is scheduled for
deletion, it is not ours to publish, and a racing game whose hero image is
somebody else's car is a weak first impression.

## Roadmap

The site's shape is driven by the game's milestones:

| Milestone | What the site becomes |
|---|---|
| Now → M4 | Landing page: what Overcut is, and a way to hear about the first playable build |
| **M5 — Time Trial** | The first releasable build. Download access and **leaderboards**, which is the first real backend |
| M8–M9 | Accounts, rankings, match history |

Nothing here needs a server runtime before M5, which is why the site is static
and why .NET Aspire is deliberately not adopted yet.

## Stack

| Piece | Choice |
|---|---|
| Framework | Astro (static output) |
| Language | TypeScript |
| Styles | Tailwind CSS |
| Lint + format | Biome |
| Runtime | Node 22 LTS, pnpm |
| Hosting | Azure Static Web Apps (free tier) |

## Local development

```bash
pnpm install
pnpm dev      # local dev server
pnpm build    # production build to dist/
pnpm check    # lint, format check, and typecheck
```

## Contributing

This project does not accept external contributions. See
[`CONTRIBUTING.md`](CONTRIBUTING.md) for why — it is a copyright question, not a
judgement about anyone's code.

## Licence

All rights reserved, source-available. See [`LICENSE`](LICENSE).
