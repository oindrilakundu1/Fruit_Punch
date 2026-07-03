# Fruit Punch Specification

## Game Rules

Fruit Punch is a two-player memory game built around fruit pairs.

- The board has 6 rows and 6 columns.
- There are 36 total tiles.
- There are 18 fruit types.
- Each fruit appears exactly 2 times.
- Players alternate turns.
- The start screen explains how to play.
- Players can choose whether Player 1 or Player 2 starts.
- On a turn, the active player reveals up to 2 hidden tiles.
- If the 2 revealed tiles are the same fruit, the player scores 30 points.
- A matched pair stays face up.
- If the 2 revealed tiles do not match, they flip back over and the turn passes.
- The game ends when all fruit pairs are found.
- The player with the higher score wins.

## Scope

Included:

- Static browser game.
- 6 by 6 tile board.
- Randomized fruit placement.
- Two-of-a-kind fruit matching.
- Two-player local gameplay.
- Score tracking.
- Turn tracking.
- End-game winner overlay.
- New Game reset.
- Rule tests.

Not included:

- Online multiplayer.
- Saved games.
- Timed mode.
- User accounts.
- Backend service.
- Persistent leaderboard.

## Functional Requirements

- The game must render exactly 36 tiles.
- The deck must include 18 fruit pairs.
- Mango must appear exactly 2 times, like every other fruit.
- The current player must be visible.
- Player 1 and Player 2 scores must be visible.
- Each player must have a distinct theme-colored score card.
- The game must show instructions before the first turn.
- The game must allow selecting the starting player before play begins.
- The board must prevent selecting already matched tiles.
- Revealing a tile should play a flip sound.
- Matching a pair should play a match sound.
- A turn must resolve after two fruit selections.
- Matching two identical fruits must award points and keep the pair open.
- Matched pairs must remain visible on the board for the rest of the game.
- Non-matching selections must flip back.
- Turns must alternate after each resolved attempt.
- The final screen must announce the winner and show a Start New Game button.

## Acceptance Criteria

- A user can play the full game locally in the browser.
- The board fits as a 6 by 6 grid on desktop and mobile-sized screens.
- The game can be reset without refreshing the page.
- Tests pass with `node --test tests/*.test.mjs`.
- The project can be served as a static site.
