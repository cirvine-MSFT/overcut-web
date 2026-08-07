# AGENTS.md — the working agreement

Short by design, and deliberately much lighter than the game repository's.

This is a static website. It has no engine, no binary assets, no local pre-flight
gate, and no weekly journal. Do not copy that ceremony here — it exists in the
game repository because Unreal cannot be built on hosted CI, and none of that
applies to a site that builds in forty seconds.

## The agreement

1. **Always open a pull request. Never push directly to `master`.**
2. **Assume everything you commit is public and permanent.** This repository is
   public. Branches are public too. Concept art, launch copy, and trailer work
   are visible the moment they land, so do not commit anything intended as a
   reveal until it is meant to be seen. Making a repository private later does
   not un-publish anything.
3. **CI must pass.** `pnpm check` locally is the same thing CI runs.
4. **Explain reasoning in the pull-request body**, not just the change. Casey is
   new to game development; the *why* is part of the deliverable.

## Facts about Overcut that constrain the copy

The game's authoritative description lives in the private game repository's
`GAME.md`. Do not restate it from memory, and do not invent details. In
particular:

- Overcut is **collisionless** — player cars never collide with one another.
- All players use **identical car performance**.
- Abilities **never** apply a negative effect to a rival.
- It is played **only from inside the car**.
- The ability system's effects, triggers, and charge model are **not decided**.
  Do not describe them as though they are.

If a page needs a claim about the game that is not already established, ask
rather than writing something plausible. Marketing copy that contradicts the
design is worse than no copy.

## Two hard content rules

- **No car imagery until the bespoke Overcut car exists.** The only vehicle in
  the game today is Epic's placeholder from the Unreal Engine templates. It is
  scheduled for deletion, it is not ours, and it is not what the game looks like.
- **Use `Overcut™` on first prominent use.** The mark is unregistered and rights
  accrue from consistent public use. This is recorded in the game repository as
  `docs/decisions/0030-licensing-and-public-disclosure.md`, decision 5.

## Build, run, test

```bash
pnpm install
pnpm dev      # local dev server
pnpm build    # production build to dist/
pnpm check    # lint, format check, and typecheck — what CI runs
```

## Scope

This repository is the website only. The game, its design records, and its
architecture decisions live elsewhere and are private. If a change you are making
needs a decision recorded, it probably belongs in the game repository's
`docs/decisions/`, not here.
