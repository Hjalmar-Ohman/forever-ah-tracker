# forever-ah-tracker

A personal, non-commercial command-line tool that tracks auction house prices on one EU WoW Forever auction house, for my own flipping analysis.

## What it does
- Takes an hourly snapshot of my auction house: lowest price, median, quantity, and estimated sales per item
- Keeps a local name/ID registry for items, with vendor sell prices
- Shows price ladders and finds listings priced below vendor sell price
- Shows all results only to me, in my own terminal. No website, no app, no data shared or published.

## Data sources and credits
- **Auction and item data:** Blizzard Battle.net API (Game Data, Forever namespaces). Blizzard Entertainment is the source of this data. This project is not affiliated with or endorsed by Blizzard Entertainment. Data from the Blizzard API is kept for at most 30 days.
- **Item and vendor data:** [ForeverDB.net](https://foreverdb.net). Every result that uses ForeverDB data shows the credit `Data: ForeverDB.net (https://foreverdb.net)`.

## Reddit (read-only, pending approval)
A planned `reddit` command shows recent community posts about the WoW Forever economy next to the price data. It's switched off until Reddit approves API access.
- **Access:** Reddit Data API with application-only OAuth (client credentials) and a descriptive User-Agent. It doesn't post, comment, vote or message.
- **Requests:** 2 read-only searches per run, at most 1 per second, typically 2–10 per hour:
  - `GET /r/woweconomy/search?q=forever&restrict_sr=1&sort=new&limit=100`
  - `GET /r/wowforever/search?q=auction OR gold OR price OR flip OR economy&restrict_sr=1&sort=new&limit=100`
- **Fields read:** title, permalink, creation time, score, comment count, and the start of the post text.
- **Data handling:** results are shown only in my own terminal and cached for at most 1 hour. They aren't shared, published, sold or used for AI/ML training, and no usernames are stored. There's no keyless or scraping fallback.

## Not included here
The tool's code, API keys and collected price data stay on my own machine. This repository only describes the project and its credits.

World of Warcraft and Blizzard Entertainment are trademarks or registered trademarks of Blizzard Entertainment, Inc.
