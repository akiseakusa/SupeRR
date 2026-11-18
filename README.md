# SupeRR Selector — Pressure Ratings

Which T20 batters and bowlers perform when the match is on the line, measured
over 199,029 deliveries from 842 IPL and T20I matches, 2022–2026.

**→ [View the report](https://akiseakusa.github.io/SupeRR/)**

## What this is

Every delivery is scored by how much it could swing the result (`leverage`) and
by how much the match itself mattered in its tournament (`stakes`, computed as
the swing in qualification probability). A player's rating is what they did on
the balls that mattered, against what a typical player does in exactly that
situation, against that quality of opposition, from that position in the order.

Every model constant is estimated from the data — shrinkage constants by
empirical Bayes, match stakes from the points table, the run value of a wicket
from the win-probability model. There is no sampling in the model, so the same
input always gives the same output.

## Reading the page

The report has two views, toggled at the top:

- **Plain English** — the rankings, what drove each player's score, season by
  season, and league cricket vs international
- **Technical** — component reliability, rank confidence intervals, the full
  signed decomposition, and the known limitations

Each ranking carries a **chance of being a real top-10 pick**: how often that
player lands in the top ten when the whole ranking is re-run on resampled
matches. Below about 50%, treat the placing as unproven.

## Honest summary

The bowler rating reproduces itself across independent splits of a player's own
matches and replicates on a season the weighting never saw. The batter rating is
weaker, and the page says so: a bowler accumulates thousands of pressure
deliveries while a batter gets a few hundred, and no amount of modelling invents
more evidence.

The page is self-contained — no network requests, no tracking, works offline.
