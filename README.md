# Infinity Pool

A dead pool prediction game for Edge Impulse. Four keyholders cast votes on who they think the next teammate to leave the nest will be — and earn points for correct predictions.

## Features

- **The Board** — Full roster with live vote tallies
- **Cast Votes** — Each voter picks their prediction for the round
- **Leaderboard** — Running score tracker (10 pts per correct pick)
- **History** — Log of all departures and who called it
- **Admin** — Manage teammates, voters, rounds, and departures
- **Access Keys** — Site is gated behind unique keys (SHA-256 hashed, not stored in plaintext)
- **Confetti** — Because correct predictions deserve celebration

## Setup

No build step. Just serve `index.html`.

```bash
# local
open index.html

# or with a simple server
python3 -m http.server 8000
```

## Access Keys

The site requires one of four unique keys to enter:

| Key                | Holder   |
|--------------------|----------|
| `EDGE-KRAKEN-9322`  | Holder 1 |
| `EDGE-SPECTER-9164` | Holder 2 |
| `EDGE-TORRENT-9500` | Holder 3 |
| `EDGE-MIRAGE-6813`  | Holder 4 |

Keys are verified client-side against SHA-256 hashes. Sessions persist per tab.

## Data Storage

All game data lives in `localStorage`. Nothing leaves the browser.

## Tech

Single HTML file. No dependencies. No framework. Vanilla JS + CSS.
