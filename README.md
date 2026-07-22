# EFYV Games

EFYV Games is the catalog and parent source-control boundary for EFYV game repositories. Each directory under [`games/`](games/README.md) owns its code, history, tests, automation, and detailed documentation as an independent Git repository.

## Available Games

| Game | Repository and documentation | Scope |
| --- | --- | --- |
| Labyrinth | [Open the Labyrinth system](https://github.com/yves-halimi-hub/labyrinth) | Unity game runtime, LabyMake designer, LabyBackend foundation, live-debug workflow, and verification suites |

## Browse The Documentation

Start with the level that matches the question:

1. [Games catalog](games/README.md) lists the available game repositories.
2. [Labyrinth system](https://github.com/yves-halimi-hub/labyrinth) explains how its three components work together.
3. [LabyBackend](https://github.com/yves-halimi-hub/labyrinth/tree/main/EFYV-labybackend), [LabyMake](https://github.com/yves-halimi-hub/labyrinth/tree/main/EFYV-labymake), and [Labyrinth runtime](https://github.com/yves-halimi-hub/labyrinth/tree/main/EFYV-labyrinth) document each component.
4. Directory and leaf READMEs inside those components describe concrete files, invariants, tests, and extension points.

## Repository Layout

```text
EFYV-games/                    parent Git repository
|-- README.md                  game catalog entry point
`-- games/
    |-- README.md              available games
    `-- labyrinth/             independent Labyrinth Git repository
        |-- README.md          Labyrinth system map
        |-- EFYV-labybackend/  shared runtime foundation
        |-- EFYV-labymake/     asset designer and live debug
        `-- EFYV-labyrinth/    Unity game and editor integration
```

## Git Boundaries

The parent repository tracks this catalog and each game as a formal Git submodule. A fresh checkout can initialize every registered game with:

```powershell
git submodule update --init --recursive
```

Each game keeps its own history and is versioned from its own directory. For example:

```powershell
git -C games/labyrinth status
```

Commit and push game changes in the game repository first, then commit the updated submodule pointer in EFYV Games. The parent therefore records the exact game revision used by the catalog while preserving the game's independent repository boundary.
