# EFYV Game Repositories

[Back to EFYV Games](../README.md)

This directory contains independently versioned EFYV games. Enter a game's README for its architecture, components, development commands, tests, and deeper documentation tree.

## Available Games

| Directory | Documentation | Components |
| --- | --- | --- |
| `labyrinth/` | [Labyrinth system README](https://github.com/yves-halimi-hub/labyrinth) | [LabyBackend](https://github.com/yves-halimi-hub/labyrinth/tree/main/EFYV-labybackend), [LabyMake](https://github.com/yves-halimi-hub/labyrinth/tree/main/EFYV-labymake), and [Unity runtime](https://github.com/yves-halimi-hub/labyrinth/tree/main/EFYV-labyrinth) |

## Navigation Pattern

Documentation becomes more specific as you descend:

```text
EFYV Games catalog
`-- games catalog
    `-- game system
        `-- component
            `-- subsystem
                `-- concrete files and contracts
```

Every new game repository should provide a root `README.md`, link back to this catalog, document its verification commands, and link its immediate subsystems. Add its entry to the table above so the entire documentation tree remains browsable from the EFYV Games root.

