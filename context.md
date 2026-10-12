# Repository Context

## What this project is

This repository contains a small, standalone **Memory Game** (also known as
Concentration). The player turns over two cards at a time and tries to find
every matching pair. It is intended to be opened and played in a web browser,
and also serves as a simple example of an interactive web page built with
vanilla HTML, CSS, and JavaScript.

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

The application is in `memory-game.html`. Its embedded CSS defines the page
layout, responsive grid, card animation, and completion dialog. Its embedded
JavaScript manages the board and game state, shuffles cards with Fisher–Yates,
handles input and matching, updates the timer and rating, and reads and writes
best scores in local storage.

`README.md` provides the quick-start instructions. To run the game, open
`memory-game.html` directly, or optionally serve the repository with a local
HTTP server and open the page there.
