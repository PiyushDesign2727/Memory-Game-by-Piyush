# Repository Context

## What this project is

This repository contains two standalone browser games built with vanilla HTML,
CSS, and JavaScript: **Memory Game** (also known as Concentration) and **Snake**.
Each game runs from its own HTML file and requires no build tools or external
dependencies.

“Memory Game” is the name and purpose of the project; the repository does not
define a separate acronym, organization, or product represented by “GHCP.”

## How to play

- Open `memory-game.html` in a modern web browser.
- Choose a 4×4 board (8 pairs) or a 6×6 board (18 pairs).
- Select two cards to reveal them. Matching pairs stay revealed; non-matches
  turn back over after a short delay.
- Match every pair to finish. The page tracks moves and elapsed time and awards
  a star rating based on the number of moves.
- Use the **Play Again** button after winning, or choose another board size to
  start a fresh game.

Cards can be selected with a mouse or by focusing them with Tab and pressing
Enter or Space.

### Snake

- Open `snake.html` in a modern web browser and press **Start game**.
- Steer with the arrow keys or W/A/S/D. On-screen direction buttons are also
  available for touch and mouse input.
- Eat apples to grow and increase your score. Avoid the walls and your own body.
- Pause or resume with the button or Space. Best score is saved in browser
  `localStorage` under `snakeBestScore`.

## Features and behavior

- A shuffled set of emoji pairs on each new game.
- Responsive 4×4 and 6×6 card grids with animated card flips.
- Move counter, elapsed-time timer, and three-star rating.
- A completion dialog with final statistics.
- A light/dark theme toggle that remembers the selected theme in browser
  `localStorage` under `memoryGameTheme`.
- A best-scores list saved in browser `localStorage` under
  `memoryGameScores`. The game keeps up to five scores, ordered by moves.
- Keyboard-operable cards, focus styling, and ARIA labels and live regions.
- No server, build step, framework, or third-party dependency is required.

## Implementation

`memory-game.html` and `snake.html` are self-contained applications. Each file
contains its own styles and game logic. The Memory Game implements the matching
board, timer, rating, theme selection, and high scores. Snake draws its board
with Canvas and handles movement, collisions, pause/resume, scoring, and its
saved best score.

`README.md` provides quick-start instructions. Open either HTML file directly,
or optionally serve the repository with a local HTTP server.

Product requirements for the theme and Snake game are documented in
`PRD_dark_theme.md` and `PRD_snake.md`.
