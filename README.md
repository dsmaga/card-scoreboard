# Card Scoreboard

A score keeper for card games. Set up the players, add a round after each deal, and the running totals stay on screen. Built for the phone that sits on the table while everyone plays, and it works just as well in a desktop browser.

The interface is available in Polish and English. Polish is the default; the PL / EN switch sits in the top right corner of every screen and remembers your choice.

## Games

**Tysiąc** — the Polish 1000. Enter one total per player each deal: tricks and marriages added up together, a failed contract written as a negative. Bombs are a single tap: the player who throws one scores nothing and everyone else gets a fixed amount (60 by default). Each player has a bomb allowance shown as small bomb icons under their score, and the button greys out once they run out. Passing 880 raises a gold *standing* flag on the board as a reminder — it never changes the points. With four players one person sits out each deal, and the app rotates who that is.

**Rummy** — plain point entry per round, with the option of fewest or most points winning and an optional score at which the game ends.

**Other game** — the same generic sheet, for anything else you play.

## What it does

- Running totals, always visible, with the leader underlined in gold
- Round-by-round history, tap any row to correct or delete it — totals recalculate from scratch
- Automatic winner detection once someone reaches the target score
- Saved games: finished ones are archived, unfinished ones wait for you to come back
- Negative values allowed everywhere
- Works offline once loaded

## Running it

Open `index.html` in any browser. That single file is the whole application — no build step, no dependencies, no accounts.

## Publishing it

To put it online with GitHub Pages, upload every file in this repository to the root of a public repository, then open **Settings → Pages**, choose **Deploy from a branch**, pick `main` and the `/ (root)` folder, and save. The address appears after a minute or two.

Keep `manifest.webmanifest` and the icon files next to `index.html`. Without them the app still runs, but Android will show a screenshot of the page instead of the app icon when someone installs it.

## Installing on a phone

Open the published address on your phone. In Safari use the share button and choose **Add to Home Screen**; in Chrome open the three-dot menu and choose **Add to home screen**. The app then launches full screen with its own icon, with no browser address bar.

## Where the scores live

Everything is stored locally in the browser, on the device you played on. Nothing is uploaded anywhere and no account is needed, which also means scores do not sync between your phone and your computer — each device keeps its own history. Clearing the browser's site data clears the saved games too.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire application: markup, styles and logic |
| `manifest.webmanifest` | Makes the app installable and full screen |
| `icon-192.png`, `icon-512.png` | Home screen icons for Android |
| `apple-touch-icon.png` | Home screen icon for iOS |
| `LICENSE` | MIT licence terms |

## Licence

Released under the MIT Licence — see [LICENSE](LICENSE). You are free to use, copy, modify and redistribute this, including commercially, as long as the copyright notice stays with it. It comes with no warranty.

## Credits

Made by DKS.
