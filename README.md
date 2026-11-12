# 🥪 ChatBLT

**The world's most confident lunch-picking artificial sandwich intelligence.**

Can't decide where to eat lunch? Give ChatBLT your zip code. It will consult the Bacon Council, toast its neural bread, and tell you exactly where to go: one random restaurant near you that's open right now. No arguments. Well, some arguments.

Don't like the pick? Hit **"Nah, something else"**. ChatBLT will find another one, and it will judge you more harshly every time.

> ChatBLT can make mistakes. So can you. Check important lunch info.
> A large percentage of statistics on ChatBLT are made up, including this one.

## Features

- A chatbot-style interface, starring a talking BLT
- Picks a random restaurant, fast-food place or café within about 3 miles of your zip code
- Only suggests places that are open right now, or that it is "63% sure" are open
- A totally scientific confidence meter and crunch rating
- Rerolls come with escalating (family-friendly) insults
- Bacon, lettuce and tomato confetti when you finally commit
- A model picker that does absolutely nothing useful

## How to use it

It's one HTML file with no build step, no dependencies and no API keys.

- **Locally:** download `index.html` and double-click it.
- **Hosted:** put `index.html` on any static host, such as GitHub Pages.
- **Shortcut:** add `?zip=12345` to the URL to jump straight to a pick.

## How it works

1. **Zip code to location:** [Zippopotam.us](https://zippopotam.us) turns the zip code into coordinates. US zip codes only.
2. **Finding restaurants:** the [Overpass API](https://wiki.openstreetmap.org/wiki/Overpass_API) finds nearby restaurants in OpenStreetMap. The page asks several public Overpass servers at once and uses whichever answers first, because they're often busy. The first search for a new area can take up to about 30 seconds. Results are cached in your browser for 12 hours.
3. **Opening hours:** a small built-in parser reads each place's OpenStreetMap `opening_hours` tag and checks it against your device's clock. Places with no listed hours may still be picked, with a warning.

Restaurant data and opening hours come from volunteers and may be out of date. Call ahead if it matters. ChatBLT is a sandwich, not a concierge.

## License and credits

- **Code:** [MIT License](LICENSE). Do whatever you want with it, just keep the copyright notice.
- **Restaurant data:** © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright), available under the Open Database License (ODbL). Keep this credit if you use the data.
- **Zip code lookup:** [Zippopotam.us](https://zippopotam.us).
