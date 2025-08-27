#### Result of 2 hour vibecoding session because didn't find good enough product. I planned to run this only locally but since it's running without any server needs, decided to publish it as simple page at https://countries-visited.pages.dev/

#### Absolutely not my proudest product since didn't check basically anything what copilot was writing but the end result very much satisfyes me.

# Visited Countries

A small client-side app to track trips by country. Click a country on the map to add visits, ratings, notes and photos. Data is stored in localStorage and can be exported/imported as JSON.

Features
- Interactive world map (D3 + TopoJSON)
- Multiple visits per country with date, rating and duration
- Local photo upload (compressed and stored as data URLs)
- Export / import JSON and clear stored data
- Per-continent counters and simple search

Run locally
1. Open `src/index.html` in a modern browser (no build step required).
2. Ensure internet access so map assets are fetched from CDN.

Data format
- Stored in localStorage key `visitedTripsV1`.
- Shape: { [countryId]: { visits: [{date, rating, days, notes, photos}], photos: [...] } }
- Export produces a JSON file suitable for import.

Notes
- Photos are embedded as data URLs in the exported JSON (keeps everything portable but increases file size).
- The app uses world-atlas CSV/TopoJSON from jsDelivr; run with network access or swap local files if needed.

Example
![Visited Countries example screenshot](example_pic.png)
