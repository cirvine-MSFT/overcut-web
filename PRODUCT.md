# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Overcut serves three audiences equally:

- sim-racing fans who want demanding competition without contact deciding their race;
- people newer to sim racing who want a fairer, more approachable entry point; and
- game-development followers interested in the progress of a solo-built playable concept.

Visitors should understand the concept on this site, then follow the development series at
<https://caseyirvine.dev> for ongoing progress.

## Product Purpose

Overcut is a playable concept for a competitive circuit racer with serious driving
fundamentals, equal machinery, team strategy, and no collisions between player cars.

The project tests whether a challenging racing game can keep the serious fundamentals of
sim racing while using lighter rules to make teamwork, strategy, and fun central. It is
the game its creator wishes existed: demanding behind the wheel without trying to
recreate every burden of the most uncompromising simulations.

## Positioning

Overcut combines four ideas:

- player cars never collide, so another driver's contact cannot end a race;
- every car has identical performance, so setup work does not create a competitive edge;
- individual driving still matters, but the team competes for the collective result; and
- drivers have distinct abilities in the broad character-ability tradition of games such
  as VALORANT, adapted to racing so they help the driver or team and never hinder rivals.

## Operating Context

The website is the public product site for Overcut. It introduces the concept and links to
the external development series. The game and its detailed design records remain in a
separate private repository.

The current website is a static, pre-launch experience. It does not provide downloads,
accounts, leaderboards, a mailing list, or release dates.

## Capabilities and Constraints

- Overcut is played only from inside the car.
- Player cars never collide with one another.
- All cars perform identically even when their liveries and visual identities differ.
- Driving errors still cost time. A barrier impact should set a driver back rather than
  erase the full investment in the race.
- Drivers have distinct abilities that create strategic choices and team roles.
- Abilities only help the driver or a teammate; they never apply a negative effect to a
  rival.
- Ability effects, triggers, charge models, and loadouts are not yet decided and must not
  be presented as settled.
- The team result is the competitive goal even though drivers also receive individual
  finishing places.
- This is a playable concept, not a promise of a fully fledged commercial game.
- The site must remain statically generated in Astro, use strict TypeScript and Tailwind
  CSS, and avoid client JavaScript unless a demonstrated need justifies it.

## Brand Commitments

- Use `Overcut™` on the first prominent use on a page.
- The Overcut wordmark uses its `O` as a racing slick: a dark tire surrounding a large
  acid-green rim. It does not use a separate cut-circle symbol.
- The visual identity is a futuristic sci-fi circuit racer with a 1985–1993 retro-cool
  register rendered in modern materials. It uses the era's confidence without synthwave
  artifacts.
- Cars, circuits, and hardware use a photoreal register. People use stylized painted
  illustration with realistic anatomy and visibly graphic surfaces.
- No Epic Unreal Engine template vehicle may appear as Overcut imagery. Only bespoke
  Overcut concept art may represent the car.
- The project should speak plainly about tradeoffs, unfinished decisions, and its
  playable-concept scope. It should not use inflated marketing claims.

## Evidence on Hand

- Accepted bespoke concept art exists for the Overcut car, livery grid, drivers, and
  Aldermoor circuit setting in the private visual-identity work.
- The public-marketing hero and supporting art were generated with Azure `gpt-image-2`
  and transferred intentionally into this public repository with sanitized provenance.
- Development writing is published at <https://caseyirvine.dev>.
- No gameplay footage, release date, testimonials, player counts, performance benchmarks,
  or finalized ability specifications are available and none may be fabricated.

## Product Principles

1. **Preserve the challenge, remove avoidable frustration.** Reward driving fundamentals
   without letting contact or setup research decide who gets to keep racing.
2. **Make competition fair by construction.** Equal car performance and non-hindering
   abilities keep the focus on driving, choices, and team execution.
3. **Make teamwork part of racing, not an afterthought.** Individual performance matters
   in service of a shared team result.
4. **Be candid about the experiment.** Overcut is a playable concept in development, and
   unsettled systems should remain visibly unsettled.
5. **Build for more people.** The project intends to represent a broad range of people
   while acknowledging that representation is a commitment to pursue, not a completed
   claim.

## Accessibility & Inclusion

- Use semantic HTML, ordered headings, and clear landmarks.
- Meet WCAG AA text contrast.
- Keep every interactive element keyboard reachable with a visible focus style.
- Respect `prefers-reduced-motion`.
- Give every published image meaningful alternative text or mark it decorative when its
  information is already present in nearby text.
- Treat representative casting as an explicit project goal while avoiding claims that
  the concept has already achieved comprehensive representation.
- The game will remain free to play and unmonetized while it uses AI-generated artwork.
  The website must disclose that use clearly and explain that AI art helps a solo
  programmer develop the concept; the disclosure should not be framed as the product's
  main subject.
