# Chess Tutor

An interactive chess tutor mobile application that teaches users how to play chess — built with .NET MAUI Blazor Hybrid.

## Goals

1. **For the user** — Learn chess through interactive lessons, puzzles, and guided gameplay on your phone
2. **For the developer (Rocky)** — Learn how to build a real-world .NET MAUI mobile application from the ground up

## Project Structure

```
Chess-Tutor/
├── src/
│   ├── ChessTutor.Core/          # Chess engine: board, pieces, move rules, game state
│   ├── ChessTutor.App/           # .NET MAUI Blazor Hybrid mobile app (Android & iOS)
│   └── ChessTutor.Api/           # ASP.NET Core Web API (puzzles, lessons, user progress)
├── tests/
│   └── ChessTutor.Core.Tests/    # Unit tests for chess logic
├── docs/
│   ├── architecture.md           # Technical design decisions
│   └── learning-notes.md         # Rocky's coding journal
└── .github/
    └── workflows/
        └── build.yml             # CI build & test pipeline
```

## Tech Stack

| Layer | Technology |
|---|---|
| Mobile App | .NET MAUI Blazor Hybrid (Android & iOS) |
| UI Components | Blazor components (Razor) |
| API | ASP.NET Core Web API |
| Chess Logic | Custom C# engine (ChessTutor.Core) |
| Testing | xUnit |
| CI | GitHub Actions |

## Why MAUI Blazor Hybrid?

- Write C# and Razor components — same skills as your Blazor learning path
- Single codebase deploys to Android and iOS
- `ChessTutor.Core` chess logic is shared and fully reusable
- No JavaScript framework to learn

## Roadmap

- [ ] Phase 1 — Core chess engine (board, pieces, legal moves)
- [ ] Phase 2 — Interactive board UI with touch support
- [ ] Phase 3 — Piece movement tutorials and highlights
- [ ] Phase 4 — Chess puzzles
- [ ] Phase 5 — Guided game with hints and explanations
- [ ] Phase 6 — Opening theory lessons

## Getting Started

> Coming soon — setup instructions will be added as the project takes shape.
