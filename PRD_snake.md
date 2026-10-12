# Product Requirements Document: Snake

## 1. Overview

Create a classic Snake game as a standalone HTML page. The player steers a
snake around a grid, eats apples to grow and score points, and avoids the walls
and its own body. The game should run locally in a modern browser without a
build step, external library, or network connection.

## 2. Goals

- Deliver a recognizable, immediately playable Snake game in `snake.html`.
- Support keyboard, mouse, and touch-friendly direction controls.
- Show the current score and persist the player's best score in the browser.
- Provide clear start, pause, resume, restart, win, and game-over states.
- Keep the board and controls usable on desktop and narrow mobile screens.
- Respect the operating system's light or dark color-scheme preference.

## 3. Non-goals

- Online multiplayer, accounts, leaderboards, or cloud score synchronization.
- Multiple levels, game modes, difficulty settings, or speed selection.
- Sound effects, external images, or third-party dependencies.
- Sharing or changing the Memory Game's score and preference data.

## 4. Target players

Casual players familiar with the classic Snake arcade game, including players
using keyboard controls on desktop and touch controls on mobile devices.

## 5. Gameplay and user experience

1. The player opens `snake.html` and sees a ready-to-play board, score, best
   score, and Start button.
2. Selecting **Start game** begins a new round with a snake on the board and an
   apple to collect.
3. The player steers the snake with arrow keys, W/A/S/D, or the on-screen
   direction buttons.
4. Each apple increases the score by 10 and adds a segment to the snake.
5. Hitting a wall or the snake's own body ends the round. Filling the entire
   board wins the game.
6. The player can pause and resume without losing the current round, or start a
   new round after a win or game over.

## 6. Functional requirements

### FR-1: Board and movement

- Render a square 24-by-24-tile game board.
- Move the snake continuously while a game is running.
- Prevent a direction change from immediately reversing the snake into itself,
  including multiple quick inputs before the next movement step.
- Keep the snake and food within the board until a collision or win.

### FR-2: Food and scoring

- Place food on an unoccupied tile.
- On collecting food, grow the snake and add 10 to the score.
- Display the current score and update the best score when it is exceeded.
- Persist the best score in browser `localStorage` under `snakeBestScore`.
- When the board is completely filled, stop play and announce a win.

### FR-3: Controls and game states

- Provide a Start button to begin or restart a round.
- Provide keyboard controls using arrow keys and W/A/S/D.
- Provide on-screen directional buttons usable with mouse and touch.
- Provide pause/resume through the Pause button and Space key.
- Ignore movement inputs when the game is not running.
- Clearly distinguish ready, running, paused, won, and game-over states and
  their available actions.

### FR-4: Accessibility and responsive layout

- Use semantic buttons with accessible names and visible keyboard focus.
- Announce score changes and terminal game status with a polite live region.
- Give the canvas an accessible description of the board and keyboard controls.
- Prevent game-direction keys from scrolling the page while playing.
- Keep all controls visible and usable without horizontal scrolling on narrow
  screens.

### FR-5: Appearance and standalone operation

- Respect the browser's light/dark color-scheme preference for the page and
  board.
- Keep the board colors, snake, and food distinguishable in both schemes.
- Implement markup, styles, rendering, and game logic within `snake.html`.
- Do not require a server, external assets, packages, or third-party scripts.

## 7. Data and compatibility

- Save only the best score and use a key dedicated to Snake.
- Do not read or overwrite Memory Game data such as `memoryGameScores` or
  `memoryGameTheme`.
- Run as a standalone page in modern desktop and mobile browsers that support
  HTML Canvas and standard browser storage.

## 8. Acceptance criteria

1. Opening `snake.html` shows the ready state and current best score.
2. Starting a round begins movement and enables pause.
3. Arrow keys and W/A/S/D steer the snake without allowing a direct reversal.
4. On-screen direction buttons steer the snake.
5. Eating an apple increases the score by 10, grows the snake, and saves a new
   best score.
6. Best score remains available after reloading the page.
7. Hitting a wall or the snake ends the game and enables restarting.
8. Pause and resume work without resetting the score or board.
9. Filling the board ends the game with a win state.
10. Theme colors follow the operating system preference and keep board pieces
    distinguishable.
11. At a narrow/mobile viewport, the board and controls fit without horizontal
    overflow.
12. The game works with no external dependency or network connection.

## 9. Manual verification checklist

- [ ] Open `snake.html` locally; confirm the ready state and board render.
- [ ] Start a game and steer with arrow keys and W/A/S/D.
- [ ] Check that a direct opposite direction is ignored.
- [ ] Steer with each on-screen directional button.
- [ ] Collect an apple and confirm the score rises by 10 and the snake grows.
- [ ] Confirm a new best score survives a reload.
- [ ] Pause and resume; confirm the round continues from the same state.
- [ ] Hit a wall and the snake's body; confirm game-over and restart behavior.
- [ ] Verify the win state when the board is full, if practical.
- [ ] Check both light and dark system appearance.
- [ ] Check a narrow mobile viewport for clipping or horizontal scrolling.
