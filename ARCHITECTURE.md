# Fruit Punch Architecture

## Technology Stack

- HTML5 for the application shell.
- CSS3 for the responsive 6 by 6 board and fruit theme.
- JavaScript ES modules for game state, rendering, and interactions.
- Web Audio API for generated flip and match sounds.
- Node.js built-in test runner for rule validation.
- No runtime dependencies.

## Architecture Overview

The project uses a static browser-game architecture.

- `index.html` defines the game header, player score panels, board container, setup screen, and winner overlay.
- `styles.css` handles the responsive layout, fruit tiles, player states, and visual style.
- `src/fruitCore.js` contains pair deck generation, seeded shuffling, turn rules, scoring, and win detection.
- `src/app.js` connects the rule engine to the DOM, handles tile interaction, and plays generated sound effects.
- `tests/fruitCore.test.mjs` validates the important non-visual rules.

## Data Model

Each tile stores:

- `id`
- `fruitId`
- `name`
- `icon`
- `type`
- `revealed`
- `matched`
- `position`

Game state stores:

- all tiles
- both players
- current player index
- selected tile IDs
- matched pair count
- turn number
- status
- winner

## Major Design Decisions

- Use real button elements for the 36 tiles so the game is accessible and touch-friendly.
- Keep the fruit rules in a separate module so deck math and scoring can be tested.
- Use 18 fruit pairs because a 6 by 6 board has 36 spaces.
- Alternate turns after every completed two-tile attempt for a clear two-player rhythm.
- Reuse the overlay for both the start instructions and the winner screen.
- Generate sound effects in the browser to avoid shipping audio files.
- Keep the project dependency-free so it can run locally or from static hosting.

## AI Tooling Used

- Codex was used for implementation, test creation, and documentation.
- The workflow used prompt interpretation, rule modeling, code generation, validation, and documentation updates.

## Agent Workflow

1. Interpreted the requested two-player fruit memory game.
2. Recalculated the board as 36 tiles and 18 fruit pairs.
3. Implemented a testable fruit pair engine.
4. Built the responsive browser UI with a setup screen.
5. Added tests for deck generation, starting player, matching, misses, and completion.
6. Updated challenge documentation for the final game.
