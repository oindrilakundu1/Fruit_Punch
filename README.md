# Fruit Punch

Fruit Punch is a two-player browser memory game where players flip fruit tiles, find matching pairs, and race for the highest score. It is built with HTML5, CSS3, and JavaScript for the AI-Native Development Challenge.

Players take turns revealing fruit tiles on a 6 by 6 board. Every fruit appears exactly two times. A player scores by finding a matching fruit pair in one turn.

A 6 by 6 board has 36 tiles, which divides cleanly into 18 fruit pairs.

## Game Description

- 6 by 6 memory board.
- 18 fruit types, each appearing exactly 2 times.
- Two local players.
- Start screen with game instructions.
- Starting player choice.
- Each turn reveals up to 2 tiles.
- Two matching fruit tiles score 30 points.
- A matched pair stays face-up on the board.
- A missed pair flips back and passes the turn.
- The game ends when every fruit pair is found.

## Setup

No install step is required. Use a modern browser, Python 3 for the local static server, and Node.js for tests.

```bash
node --test tests/*.test.mjs
```

## Run

```bash
python3 -m http.server 4173
```

Open:

```text
http://localhost:4173
```

If npm is available, the same commands are also available as:

```bash
npm test
npm start
```

## Project Structure

```text
.
├── index.html
├── styles.css
├── package.json
├── src
│   ├── app.js
│   └── fruitCore.js
├── tests
│   └── fruitCore.test.mjs
├── SPEC.md
├── ARCHITECTURE.md
└── RETROSPECTIVE.md
```

## Current Status

- Playable two-player memory game
- 6 by 6 responsive tile board
- Randomized fruit placement
- 18 fruit pairs
- Start instructions and player choice
- Turn-based player scoring
- Theme-colored player cards
- Flip and match sound effects
- Winner announcement with Start New Game button
- Fruit-themed visual style
- Deterministic rule tests
