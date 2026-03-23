# Chess Tutor

An interactive chess tutor application that teaches users how to play chess — built with Blazor and .NET.

## Goals

1. **For the user** — Learn chess through interactive lessons, puzzles, and guided gameplay
2. **For the developer (Rocky)** — Learn how to build a real-world .NET/Blazor application from the ground up

## Project Structure

```
Chess-Tutor/
├── src/
│   ├── ChessTutor.Core/          # Chess engine: board, pieces, move rules, game state
│   ├── ChessTutor.Web/           # Blazor WebAssembly front-end (interactive board UI)
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
| UI | Blazor WebAssembly |
| API | ASP.NET Core Web API |
| Chess Logic | Custom C# engine (ChessTutor.Core) |
| Testing | xUnit |
| CI | GitHub Actions |

## Roadmap

- [ ] Phase 1 — Core chess engine (board, pieces, legal moves)
- [ ] Phase 2 — Interactive board UI in Blazor
- [ ] Phase 3 — Piece movement tutorials and highlights
- [ ] Phase 4 — Chess puzzles
- [ ] Phase 5 — Guided game with hints and explanations
- [ ] Phase 6 — Opening theory lessons

## Getting Started

> Coming soon — setup instructions will be added as the project takes shape.
