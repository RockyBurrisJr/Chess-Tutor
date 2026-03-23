# Architecture

> This document evolves as we make decisions. Updated as we go.

## High-Level Design

```
[ Browser ]
    |
[ Blazor WebAssembly (ChessTutor.Web) ]
    |            |
[ Core Logic ]  [ HTTP API calls ]
(ChessTutor.Core)      |
                [ ASP.NET Core API (ChessTutor.Api) ]
```

## ChessTutor.Core

The heart of the application. Pure C# with no dependencies on UI or infrastructure.

Responsibilities:
- Board representation (8x8 grid)
- Piece types and movement rules
- Legal move generation
- Check / checkmate / stalemate detection
- Game state management (FEN support planned)

## ChessTutor.Web

Blazor WebAssembly project. Renders the chess board, handles user interaction, drives lessons.

## ChessTutor.Api

ASP.NET Core Web API. Will serve puzzles, lessons, and eventually persist user progress.

## Key Design Decisions

| Decision | Choice | Reason |
|---|---|---|
| UI framework | Blazor WASM | Consistent with Rocky's Blazor learning path |
| Chess logic | Custom engine | Learning purpose — understanding the rules by coding them |
| Test framework | xUnit | .NET standard, good IDE integration |
