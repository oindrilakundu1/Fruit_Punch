# Fruit Punch Retrospective

## AI Tools Used

- Codex for planning, implementation, validation, and documentation.

## Development Workflow

The workflow followed the AI-native development challenge lifecycle:

1. Translate the game idea into precise rules.
2. Recalculate the board: 36 tiles divides into 18 pairs.
3. Update the game to pair matching.
4. Implement a small testable rules module.
5. Build the browser UI.
6. Validate with syntax checks and rule tests.
7. Update the required challenge documents.

## What Worked Well

- Separating `fruitCore.js` from the DOM made the game rules easy to test.
- The 6 by 6 board works well with CSS Grid and makes the game easier to finish.
- Button-based tiles give the game good mouse, touch, and keyboard behavior.
- Generated sound effects added feedback without adding asset files.
- The start screen makes the rules clearer before the first move.
- AI was helpful for turning a loose game concept into a complete ruleset.

## What Did Not Work Well

- The 6 by 6 version avoids leftover tiles because 36 divides cleanly into pairs.
- The smaller board still needs careful responsive sizing, especially on small screens.
- Emoji availability can vary slightly by platform.

## Surprises and Discoveries

- The 6 by 6 recalculation simplified the rules and made the game faster to play.
- Two-card matching is quicker to understand and easier to finish in a short demo.
- Testing deck composition catches mistakes that would be annoying to find by manual play.

## Estimated Percentage of AI-Generated Code

Approximately 90 percent of the initial implementation and documentation was AI-generated, with human review recommended for visual polish and gameplay balance.

## Time Spent

Initial implementation target: about 1 to 2 hours for a playable version, tests, and documentation.

## What I Would Do Differently Next Time

- Add difficulty modes with smaller boards.
- Add optional sound and animation settings.
- Add local high-score or match-history storage.
- Run more playtesting to tune scoring.

## Key Lessons Learned

- AI performs best when ambiguous rules are converted into explicit constraints.
- Small pure functions make game rules much easier to validate.
- Responsive board games need layout decisions early.
- Documentation helps explain design tradeoffs, especially when requirements need interpretation.
