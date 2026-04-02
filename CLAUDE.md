# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## About

Starter project for a Claude Code course on [codewithmosh.com](https://codewithmosh.com/p/claude-code). The app is intentionally buggy with poor UI and messy code — changes should be made as part of the course exercises.

## Commands

```bash
npm run dev      # Start dev server at http://localhost:5173
npm run build    # Production build
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

## Architecture

Single-component React app (`src/App.jsx`) with no routing or state management library. All state lives in `App` via `useState`. No tests are set up.

- `src/App.jsx` — all application logic and JSX
- `src/App.css` — component styles
- `src/index.css` — global styles

## Known Bugs (intentional)

- Transaction `amount` is stored as a string; arithmetic on it produces string concatenation instead of numeric sums.
- Transaction #4 ("Freelance Work") is marked `type: "expense"` but should be `"income"`.
