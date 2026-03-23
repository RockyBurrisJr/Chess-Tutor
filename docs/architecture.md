# Architecture

> This document evolves as we make decisions. Updated as we go.

## High-Level Design

```
[ Android / iOS Device ]
         |
[ .NET MAUI Shell (ChessTutor.App) ]
         |                  |
[ Blazor Components ]   [ HTTP API calls ]
         |                  |
[ ChessTutor.Core ]   [ ASP.NET Core API (ChessTutor.Api) ]
  (chess engine)        (puzzles, lessons, user progress)
```

## ChessTutor.Core

The heart of the application. Pure C# class library with no dependencies on UI or infrastructure.

Responsibilities:
- Board representation (8x8 grid)
- Piece types and movement rules
- Legal move generation
- Check / checkmate / stalemate detection
- Game state management (FEN support planned)

This is referenced by both `ChessTutor.App` and `ChessTutor.Api`, so the chess logic lives in exactly one place.

## ChessTutor.App

.NET MAUI Blazor Hybrid project. The mobile app shell that hosts Blazor components inside a native container.

- MAUI handles the native mobile lifecycle (permissions, screen, touch events)
- Blazor Razor components handle all UI rendering
- Targets Android and iOS from a single project

## ChessTutor.Api

ASP.NET Core Web API. Optional backend that will serve puzzles and lessons, and eventually persist user progress across devices.

## Key Design Decisions

| Decision | Choice | Reason |
|---|---|---|
| Mobile framework | .NET MAUI Blazor Hybrid | Deploys to Android & iOS; reuses Rocky's Blazor skills |
| Chess logic | Custom engine (ChessTutor.Core) | Learning purpose — understand the rules by coding them |
| Shared logic | Class library referenced by App + Api | Single source of truth for chess rules |
| Test framework | xUnit | .NET standard, good IDE integration |
