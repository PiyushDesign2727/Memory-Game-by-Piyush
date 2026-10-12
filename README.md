# Memory Game and Snake

Two lightweight, standalone browser games built with plain HTML, CSS, and
JavaScript. Open either game directly in a modern browser—no installation,
build step, or external dependency is required.

## Games

### Memory Game

Match all the emoji pairs on a **4×4** or **6×6** board.

- Flip cards with a mouse or with **Tab** and **Enter/Space**.
- Track moves, elapsed time, and a move-based star rating.
- Switch between light and dark themes; the choice is saved in the browser.
- View your five best scores.

Open [`memory-game.html`](memory-game.html) to play.

### Snake

Steer the snake around the board, eat apples to grow, and avoid the walls and
your own body.

- Use the **arrow keys** or **W/A/S/D** to steer.
- Use the on-screen direction buttons for mouse or touch input.
- Pause or resume with the button or **Space**.
- Earn 10 points per apple and keep a personal best score.
- The page follows your operating system's light/dark color preference.

Open [`snake.html`](snake.html) to play.

## Run locally

### Open directly

Open either HTML file in a modern web browser. Game scores and preferences are
saved in that browser's local storage.

### Use a local web server (optional)

From the project directory, run:

```bash
python -m http.server 8000
```

Then visit:

- Memory Game: <http://localhost:8000/memory-game.html>
- Snake: <http://localhost:8000/snake.html>

## Project files

| File | Description |
| --- | --- |
| [`memory-game.html`](memory-game.html) | Memory card game, styles, and game logic |
| [`snake.html`](snake.html) | Snake game, canvas rendering, styles, and game logic |
| [`context.md`](context.md) | Project purpose, features, and implementation overview |
| [`PRD_dark_theme.md`](PRD_dark_theme.md) | Dark-theme requirements and verification checklist |
| [`PRD_snake.md`](PRD_snake.md) | Snake requirements and verification checklist |

## Technical notes

- Both games are self-contained HTML files with embedded CSS and JavaScript.
- There are no external libraries, services, or assets.
- Memory Game storage keys: `memoryGameTheme` and `memoryGameScores`.
- Snake best-score storage key: `snakeBestScore`.
- Browser storage is local to the browser and device; it is not synchronized.

## Repository

Clone this repository with:

```bash
git clone https://github.com/PiyushDesign2727/Memory-Game-by-Piyush.git
cd Memory-Game-by-Piyush
```
