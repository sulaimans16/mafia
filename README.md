# Mafia — Role Card Dealer

Pass-and-play web app for the party game Mafia. Pick the number of players, shuffle, and pass the phone around — each player taps to see their secret card (Mafia, Doctor, Detective or Civilian).

## Role distribution (auto)
| Players | Mafia | Doctor | Detective | Civilians |
|---|---|---|---|---|
| 4–7 | 1 | 1 | 1 | rest |
| 8–11 | 2 | 1 | 1 | rest |
| 12–15 | 3 | 1 | 1 | rest |
| 16–19 | 4 | 1 | 1 | rest |
| 20 | 5 | 1 | 1 | rest |

Mafia = max(1, floor(players / 4)). Toggle **Custom** to change the counts.

## Features
- 4–20 players, cryptographically random shuffle (`crypto.getRandomValues`)
- Optional player names; mafia members see their partners
- Narrator sheet behind a 1-second hold so nobody peeks
- Single static `index.html`, no build step — deploys as-is on Vercel

## Offline / install
The app is a PWA. Open it once while online; after that it loads and deals cards with no internet.
Add it to your home screen (Chrome: menu → *Install app*; Safari: Share → *Add to Home Screen*) to use it like a native app.
Fonts are self-hosted in `fonts/` (Inter and Playfair Display, SIL Open Font License). When changing any file, bump `VERSION` in `sw.js`.
