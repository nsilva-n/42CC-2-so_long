# so_long

*Oh noble voyager, chart your course through the labyrinth of pixels and code, where the hero’s journey unfolds, one tile at a time!*

Within this repository lies **so_long**, a tale spun in the language of C, where you shall craft an adventure game. A journey that blends the artistry of game design with the rigor of algorithms, challenging you to guide a character through obstacles, collect treasures, and find their way to freedom.

## Prelude

*Oh brave dreamer, venture into the realm of `so_long`, where the boundaries of creativity and logic merge!*

In this project, you shall breathe life into a simple 2D game using the MiniLibX graphical library. Each step is a dance with challenges, where memory must be managed, and every pixel tells a story.

## Table of Contents

- [The Quest](#the-quest)
- [Features](#features)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [Game Mechanics](#game-mechanics)
- [Testing](#testing)
- [Acknowledgments](#acknowledgments)

## The Quest

*Embark, O valiant coder, on this odyssey of pixels and logic!*

Your mission is to design a 2D game, adhering to these sacred tenets:
1. **The Labyrinth**: Create a rectangular map where the hero must navigate through walls, pitfalls, and treasures.
2. **The Treasures**: Collect all items before reaching the exit.
3. **The Exit**: Lead the hero to freedom through the designated portal.
4. **The Journey**: Display the game window using MiniLibX, where every move is counted and displayed.

This is a journey of both skill and imagination, where you weave together the threads of C programming and game design.

## Features

*Behold the marvels of so_long:*

- **Dynamic Map Rendering**: A living world, rendered tile by tile, using the MiniLibX library.
- **User Input**: Guide the hero using keyboard controls to navigate the map.
- **Collision Mechanics**: Prevent the hero from walking through walls or into the abyss.
- **Victory and Defeat**: Achieve triumph by collecting all treasures and escaping, or taste defeat by succumbing to the perils of the labyrinth.

## Requirements

*To embark on this journey, equip yourself with these tools:*

- **Compiler**: GCC or Clang.
- **Libraries**: MiniLibX (included in the repository).
- **Dependencies**:
  - X11 (XQuartz for MacOS, Xorg for Linux).
  - Development tools such as `gcc`, `make`, and `libbsd-dev`.
  - Example installation for Ubuntu/Debian:  
    ```bash
    sudo apt-get install gcc make xorg libxext-dev libbsd-dev
    ```

## Getting Started

*Gather your courage and take the first steps!*

Clone this repository and navigate to the `so_long` directory:
```bash
git clone https://github.com/nsilva-n/42CC-2-so_long.git
cd 42CC-2-so_long
make
```

Run your program with:
```bash
./so_long <path_to_map_file>
```

Example:
```bash
./so_long maps/level1.ber
```

## Game Mechanics

*The dance of the hero is guided by these rules:*

### Map File
- The map must be a `.ber` file, formatted as a rectangular grid of characters:
  - `1`: Wall
  - `0`: Empty space
  - `C`: Collectible
  - `E`: Exit
  - `P`: Player starting position

Example:
```
11111
1P0C1
10001
1C0E1
11111
```

### Controls
- **W/A/S/D**: Move the player up, left, down, and right.
- **ESC**: Quit the game.

### Objectives
- Collect all the treasures (`C`) before reaching the exit (`E`).
- Avoid walking through walls (`1`).

*Each move is a step closer to victory or despair!*

## Testing

*Test thy creation to ensure it withstands the trials of the labyrinth:*

### Example Maps
Create map files and test various scenarios:
- Single exit, multiple collectibles.
- Maps with invalid characters or improper formatting.
- Large maps to test rendering performance.

### Debugging
Run your program with a debugger to ensure memory is managed correctly:
```bash
valgrind --leak-check=full ./so_long maps/level1.ber
```

### Visualization
To explore the graphical output, ensure you have the X11 server running:
```bash
export DISPLAY=:0
./so_long maps/level1.ber
```

## Acknowledgments

*With profound gratitude to the creators of MiniLibX, the 42 curriculum, and the pioneers of game design, we dedicate this work.*

May your journey through the labyrinth of `so_long` lead you to mastery in both art and logic.
