# Alien Invasion

A 2D arcade game built with Python and Pygame while working through *Python Crash Course* (SIWES II training).

**Play it in your browser:** https://olakeys-alien-invasion.netlify.app
(the first load takes around 30 seconds while the Python runtime downloads; click the screen to start)

## How to play

- **Play button** or **P**: start a new game
- **← / →**: move the ship
- **Space**: fire
- **Q**: quit (desktop only)

Destroy the whole fleet before it reaches you. Each new fleet is faster and worth more points. You have three ships.

## Project structure

| File | Responsibility |
|---|---|
| `main.py` | Starts the game and runs the main loop |
| `settings.py` | Screen size, colours, speeds and scoring settings |
| `ship.py`, `alien.py`, `bullet.py` | The game objects (Pygame sprites) |
| `game_functions.py` | Event handling, collisions, fleet creation and screen updates |
| `game_stats.py`, `scoreboard.py` | Score, level, high score and ships left |
| `button.py` | The Play button |

## Running it

On your computer:

```bash
pip install pygame-ce
python main.py
```

In the browser, the game is packaged with [pygbag](https://github.com/pygame-web/pygbag), which runs Python in WebAssembly. The main loop is an `async` function that calls `await asyncio.sleep(0)` once per frame so the browser stays responsive.

```bash
pip install pygbag
python -m pygbag --build alien_invasion
```
