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

## Not included here
The tool's code, API keys and collected price data stay on my own machine. This repository only describes the project and its credits.

World of Warcraft and Blizzard Entertainment are trademarks or registered trademarks of Blizzard Entertainment, Inc.
