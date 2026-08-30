# Changelog

## 1.0.0 — first release

Everything below works offline and saves to the browser it's opened in.

### Formats and games

- Singles and doubles across 8-ball, 9-ball racks, 10-ball and 9-ball points.
- Team night for 8-ball and 9-ball.
- Three levels of detail — simplified, detailed and league — picked on the way
  into a match so league races fill as skill levels are entered.
- League mode only where a league exists: 8-ball and 9-ball points. It locks the
  races to the chart and assumes winner breaks.

### Scoring

- Rack races for 8-ball, 9-ball and 10-ball: tap who won, count to the race.
- 9-ball points ball by ball — one tap to score, two for dead, three to clear.
  Potting the 9 kills whatever is left on the table.
- Innings counted from a miss button, ticking when the second player's turn ends.
- Defensive shots per player.
- Points on the break, 9 on the snap and break and run for 9-ball.
- 8-ball Game Over sheet with every way a game ends, including a stalemate that
  voids the rack. Break outcomes are only offered while it's still the break.
- Match points: the APA chart for 9-ball, and for 8-ball straight off the score —
  a shutout is 3-0, the loser reaching the hill is 2-1, anything between is 2-0.

### Breaking

- Winner breaks, alternate breaks or loser breaks, plus who broke first.
- Who breaks next is derived from the rule and the racks played rather than
  stored, so undo can't leave it out of step. A voided rack is stepped over.

### Races

- APA 8-ball games-must-win grid and 9-ball points required to win, loaded in one
  click and shown read-only until you choose to edit them.
- Doubles averages the pair rounded up for the 8-ball grid, and combines them for
  the 9-ball doubles chart.

### Team night

- Eight roster slots a side, blanks allowed, with a Here/Out toggle.
- Rosters save per game and reload with last week's skill levels.
- Match tabs across the top, so two matches can be scored at the same time.
- Picking both players opens the scorer; recording writes the match points back.
- The 23 rule checked as a projection — a pick is refused when it would leave no
  legal way to finish, with the reason attached.
- Two Senior Skill Level players a team match.
- A rostered player who isn't at the venue still counts toward the limit.
- Warnings before the night starts for a roster that has to play four to 19 or
  three to 15.
- Sudden death for tournament play — called by the director, applying to every
  match not yet recorded, two points for the first rack and one for the second.

### Theory

- Every legal lineup for the matches remaining, for either team.
- Must-play, optional and can't-fit, plus how many of the legal lineups each
  player appears in — so a player in twelve of thirteen reads differently from
  one who is genuinely compulsory.
- Lock a player in or take them out to model it, without touching the night.

### Housekeeping

- Every match saves separately and survives leaving and coming back.
- Undo opens a labelled list of recent actions — step back to any of them rather
  than tapping undo repeatedly.
- Clear a saved match from its tile on the menu.
- Installs to a phone or desktop and runs with no connection.
