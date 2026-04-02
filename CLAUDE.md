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

React app with no routing or state management library. The `transactions` array lives in `App` and is passed down as props. No tests are set up.

- `src/App.jsx` — holds the `transactions` state and `handleAdd`; renders the three child components
- `src/Summary.jsx` — computes and displays income, expenses, and balance from `transactions` prop
- `src/TransactionForm.jsx` — owns its own form state; calls `onAdd(transaction)` prop on submit
- `src/TransactionList.jsx` — owns filter state; receives `transactions` prop and renders the filtered table
- `src/App.css` — component styles
- `src/index.css` — global styles

## Known Bugs (intentional)

- Transaction #4 ("Freelance Work") is marked `type: "expense"` but should be `"income"`.
