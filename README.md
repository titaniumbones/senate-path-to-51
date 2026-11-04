# Senate Path to 51

All 35 U.S. Senate seats on the 2026 ballot, ranked by the New York Times live forecast's chance of a Democratic win, with a line at the 51st seat. Democrats hold 34 seats not up this year, so they need the top 17 races to reach 51. Republicans keep control at 50 through the vice president's tiebreak.

Live site: https://titaniumbones.github.io/senate-path-to-51/

## Updating the numbers

All data lives in [`data/races.json`](data/races.json). The page reloads it every 60 seconds.

**From the page (fastest):**
1. On the NYT Live Forecast page, click **Show all races** under *Key Senate races*, then copy the table from "Last updated" down through Wyoming.
2. Paste it into **Update from the NYT forecast** at the bottom of the site, check the preview, and click **Apply**. You can also click any race to edit it or call it by hand.
3. Click **Publish to site** in the bar that appears. The first time, paste a [fine-grained GitHub token](https://github.com/settings/personal-access-tokens/new) limited to this repository with **Contents: Read and write**. The token stays in that browser's localStorage.

Edits stay in your browser until you publish them. Other viewers see them after GitHub Pages redeploys, usually within a minute.

**By hand:** edit `data/races.json` on GitHub and commit.

## Data fields

`races` is keyed by postal code. `prob` is the Democratic (or, for Nebraska, non-Republican) win chance from 0 to 100. ">95%" is stored as 97 and "<5%" as 3. `status` is `open`, `D`, `R` or `I` (called). `marginD` is the NYT's estimated final margin, positive for Democrats, and breaks ties in the ranking. `meta.dNotUp` and `meta.rNotUp` are the seats not on the ballot.

Source: NYT Live Forecast and Senate results pages (race calls from the AP).
