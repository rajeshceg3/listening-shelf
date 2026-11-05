# the listening shelf

A small, opinionated shelf of podcasts worth your hours on AI engineering, LLMs and
inference. Every pick carries its evidence - the primary source (episode page, show notes
or transcript) saying what you will learn, and, labeled separately, the community threads
that recommend it.

**Live:** https://rajeshceg3.github.io/listening-shelf/

## What it does

- Eight picks, grouped: the featured episode, the core shelf, agents in production, the daily pulse.
- Each card: what you learn (from the primary source), evidence links, and a starter episode.
- "Play in YouTube Music" opens the episode in YouTube Music on the web where the show
  publishes full episodes to YouTube; whether a phone hands the link to the app is up to
  the device. Other buttons go to the show's own page.
- "Listened" marks live in `localStorage` - they stay on your device. No account, no tracking.

## Verification notes (create-verification)

Exercised in a real browser (cloud Chrome) at 390px and 1280px with inspected screenshots:

- `shelf: tally 0/8 -> toggle listened -> card dims + stamp + tally n/8 -> persists on reload -> untoggle restores`
- Play links: YouTube Music video IDs title-checked against YouTube oEmbed
  (Movva uyzqxIoiobU, Karpathy lXUZvyajciY, Shanahan ztNdagyT8po, Knoop SSA8vNrFpXI);
  show/channel links return HTTP 200.
- Evidence links resolve to the named thread, episode or show page.
- Episode substance quotes/claims come from the linked primary source, not the community threads.

States: `fresh -> partially-heard -> all-heard`; transitions only via the listened toggles.
No backend; single static page, no runtime dependencies except Google Fonts.

## Stack

Single `index.html`. Fraunces + Caveat, warm paper palette, clay controls.
