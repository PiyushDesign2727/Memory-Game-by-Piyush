# Product Requirements Document: Dark Theme

## 1. Overview

Add a dark visual theme to the Memory Game so players can choose a comfortable
appearance in bright or low-light environments. The theme must work throughout
the game and must not change how the game is played or how existing scores are
stored.

The game is a standalone HTML, CSS, and JavaScript page in
[`memory-game.html`](./memory-game.html), with 4×4 and 6×6 boards, keyboard and
mouse controls, a timer, moves, a rating, a completion dialog, and saved best
scores.

## 2. Problem and opportunity

The game currently uses a light appearance. Players who prefer a darker
interface or play in low-light conditions need a way to switch themes without
losing game progress or existing best scores.

## 3. Goals

- Let players switch between light and dark themes at any time.
- Make the selected theme legible and visually consistent across the entire
  game page.
- Remember the player's choice between visits using browser storage.
- Preserve the current game mechanics, accessibility, responsive layout, and
  saved high scores.
- Keep the game standalone, with no external service or dependency required.

## 4. Non-goals

- Automatically follow the operating system theme.
- Add additional themes or user-configurable colors.
- Change card symbols, scoring, rating thresholds, board sizes, or game rules.
- Add an account or synchronize preferences between devices.
- Redesign the game beyond the styling needed for the two themes.

## 5. Users

Players of the Memory Game who want to choose a light or dark appearance,
including players using the game in low-light environments and players who
operate it with a keyboard.

## 6. User experience

A clearly labeled theme control appears near the existing game controls. It
communicates whether dark theme is on or off, can be operated by mouse or
keyboard, and updates the page immediately when activated. Changing the theme
does not restart the game, change the selected board size, or alter moves,
timer, matches, or saved scores.

If the player has not selected a theme before, the game opens in its existing
light appearance. A saved preference is applied when the game opens again.

## 7. Functional requirements

### FR-1: Theme toggle

- Provide one keyboard-operable button to toggle between light and dark themes.
- The button's visible label and pressed state must accurately reflect the
  active theme.
- Activating the control applies the new theme immediately without reloading
  the page or resetting the current game.

### FR-2: Theme coverage

Both themes must provide readable foreground/background contrast and consistent
styling for:

- The page background and primary text.
- Statistics, board-size controls, and theme control.
- Face-up, face-down, focused, and matched cards.
- Best-score panel and score text.
- The game-completion dialog and its contents.

Interactive states, including hover, keyboard focus, and active board-size
selection, must remain distinguishable in both themes. Card-flip animations
must continue to work.

### FR-3: Persistence and default

- Save the player's explicit choice in browser `localStorage`, separately from
  game scores.
- Restore that choice on a later visit to the page.
- Use the light theme when no saved preference exists.
- Do not clear, overwrite, or otherwise modify the existing best-score data
  when changing themes.

### FR-4: Accessibility and responsive behavior

- The toggle must be a semantic button with an accessible name and a state
  exposed to assistive technology, such as `aria-pressed`.
- Preserve visible keyboard focus and the existing keyboard operation of cards
  and controls.
- Keep the control and both themes usable at the existing mobile and desktop
  layouts.

## 8. Compatibility and constraints

- Implement within the existing standalone page and its embedded styles and
  script unless there is a concrete reason to change that structure.
- Do not introduce frameworks, packages, network requests, or a build step.
- Preserve the current light-theme appearance as the default for players with
  no saved preference.
- Preserve the existing score-storage key and game behavior.

## 9. Acceptance criteria

The feature is accepted when all of the following are true:

1. A new or first-time visitor sees the light theme and a theme control showing
   the current state.
2. Activating the control switches the whole game page to dark theme; activating
   it again restores light theme.
3. The theme control's label and accessible pressed state stay synchronized
   with the displayed theme.
4. Reloading or reopening the page restores the last explicitly selected
   theme.
5. Switching themes during a game leaves the board, current moves, elapsed
   time, match state, and board size unchanged.
6. Both themes remain legible and styled consistently on the game board,
   statistics, controls, score list, and completion dialog.
7. The game remains playable using mouse and keyboard, and the card flips,
   mismatch delay, timer, rating, win flow, replay, and board-size selection
   continue to work.
8. Existing best scores remain present and usable after changing themes and
   reloading the page.
9. No external dependency or network connection is required to use the theme.

## 10. Manual verification checklist

After implementation, open `memory-game.html` in a browser and verify:

- [ ] The initial theme is light when no preference has been saved.
- [ ] The toggle switches to dark and back without a page reload.
- [ ] The button label and pressed state match the active theme.
- [ ] The choice is still active after reloading the page.
- [ ] A partially played game keeps its board and statistics when the theme
      changes.
- [ ] Both board sizes, face-up and matched cards, and keyboard focus are
      visible in both themes.
- [ ] The best-scores section and game-completion dialog use the active theme.
- [ ] Mouse and keyboard gameplay, replay, timer, rating, and score saving still
      work.
- [ ] The layout remains usable at a narrow/mobile viewport.

## 11. Current implementation note

The page already contains a light/dark toggle and saves the selected theme in
`localStorage` under `memoryGameTheme`. This PRD records the intended product
behavior and acceptance criteria for completing and verifying that feature;
it is a requirements document, not a request to change the game implementation.
