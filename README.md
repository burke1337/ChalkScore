# ChalkScore

Pool scorekeeping that works in a basement with no signal. 8-ball, 9-ball and
10-ball, singles, doubles and APA team nights, in one page you can install on a
phone and forget about.

Three levels of detail, so the same app suits a Saturday tournament and a
Thursday league night:

- **Simplified** — the score and who breaks next. Nothing else to tap.
- **Detailed** — adds innings from a miss button, defensive shots and break stats.
- **League** — adds match points, locks the races to the APA chart, winner breaks.

---

## Run it

Open `index.html`. That's the whole app — no server, no install, no build step.

Everything saves to the browser as you go. Leaving a match, closing the laptop or
switching games never costs you a rack, and each game keeps its own match.

---

## Put it online (GitHub Pages)

1. Make a new repository on GitHub.
2. Push these four files to it:

   ```
   index.html
   sw.js
   manifest.webmanifest
   icon.svg
   ```

3. **Settings → Pages**, Source **Deploy from a branch**, branch `main`, folder
   `/ (root)`, then **Save**.
4. A minute later it's at `https://<your-username>.github.io/<repo-name>/`

Once it has loaded online once it caches itself and opens with no connection.
On iPhone, Share → Add to Home Screen. On Android, menu → Install app.

If you publish an update, bump `CACHE` in `sw.js` (`chalkscore-v1` → `-v2`) so
installed copies pick it up instead of serving the cached one.

---

## What it does

### The games

**8-ball, 9-ball racks and 10-ball** are the same engine — tap who won, count to
the race. **9-ball points** is ball by ball: one tap gives the ball to whoever is
at the table, a second marks it dead, a third clears it, and potting the 9 kills
whatever is left.

### Breaking

Winner breaks, alternate breaks or loser breaks, plus who broke first. Who's up
next is worked out from the rule and the racks played rather than stored, so
undoing a rack can never leave the break out of step with the score. A stalemate
voids the rack and leaves the same player breaking.

### 8-ball game outcomes

In detailed and league, a Game Over sheet records how the game actually ended:
made the 8, break and run, 8 on the break, 8 out of turn, made the 8 and
scratched, 8 on the break and scratched, or a stalemate. Losses hand the game to
the opponent, pass the turn and score an inning when it was the second player.
The three break outcomes only appear while it's genuinely still the break.

### Races

APA charts load in one click. 8-ball uses the games-must-win grid; 9-ball uses
points required to win. Doubles averages the pair rounded up for 8-ball and
combines them for the 9-ball chart. Under league the races come off the chart and
can't be hand-edited.

### Team night

Five singles matches, eight roster slots a side, blanks allowed. Match tabs run
across the top so two matches can be scored at once. Picking both players drops
straight into the scorer, and recording the result writes the match points back.

The rules it watches for you:

- **23 rule** — the team skill limit across all five matches, checked as a
  projection so a pick is refused when no legal completion remains.
- **Senior Skill Level** — 6 and up, two to a team match.
- A player goes in once a night.
- A rostered player who isn't at the venue still counts toward the limit, so a
  forfeited seat isn't free.

Rosters save per game and reload next week with last week's skill levels ready to
adjust.

### Theory

Every legal way to fill the matches you have left, for either team. Shows who is
genuinely compulsory rather than assumed, how often each player appears across
the legal lineups, and which lineups use the full 23. Lock a player in or take
them out to model it. It's a sandbox — nothing there touches the night.

---

## Change something

`index.html` is the source. One file, no build step, no dependencies. Open it in
an editor and the whole app is there.

---

## A note on the numbers

This is an unofficial helper. The charts and rules are the ones used in APA Open
divisions, and they're editable outside league mode because rooms run things
differently. The paper scoresheet is still what counts.

---

## License

Do what you like with it.
