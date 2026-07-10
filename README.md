# Connect_Four_Game
A feature-rich Connect Four game built with Python and Pygame CE, featuring PvP &amp; AI modes, 3 difficulty levels, minimax with alpha-beta pruning, particle effects, sound, animations, score tracking, and smooth keyboard/mouse controls.
# Connect Four Game

A feature-rich Connect Four board game built with **Python** and **Pygame**.

## Features

- **2 Game Modes** - Player vs Player (local) and Player vs AI
- **3 AI Difficulty Levels** - Easy, Medium, Hard (minimax algorithm)
- **Keyboard Controls** - Use arrow keys + D key to play
- **Particle Effects** - Confetti on win, background starfield
- **Sound Effects** - Programmatic audio (drop, win, draw)
- **Score Tracking** - Persists across rounds within a session
- **Animated Menu** - Mode and difficulty selection with keyboard/mouse
- **Glowing Board** - Winner cells pulse and highlight
- **Gradient Background** - Dynamic visual theme

## How to Play

1. Select game mode (PvP or PvAI) and difficulty from the menu
2. Use LEFT/RIGHT arrow keys or mouse to select a column
3. Press D key or click to drop your piece
4. First to connect **4 in a row** (horizontal, vertical, or diagonal) wins

## Controls

| Key / Action | Function |
|---|---|
| LEFT / RIGHT Arrow | Select column |
| D Key | Drop piece |
| Mouse Move | Select column |
| Left Click | Drop piece / Select menu option |
| R | Restart game |
| M | Return to menu |
| ESC | Quit / Back to menu |
| UP / DOWN (Menu) | Change game mode |
| LEFT / RIGHT (Menu) | Change AI difficulty |
| ENTER | Start game |

## Installation

1. Make sure you have Python 3.x installed
2. Install dependencies:
   ```
   pip install pygame-ce numpy
   ```
3. Run the game:
   ```
   python main.py
   ```

## Project Structure

```
Connect four game/
├── main.py        # Entry point (run this)
├── config.py      # Constants, colors, screen setup, fonts
├── sounds.py      # Sound generation & playback
├── effects.py     # Particle & Star classes
├── board.py       # Board logic (create, drop, win check)
├── ai.py          # AI logic (evaluation & minimax)
├── renderer.py    # All drawing functions
├── game.py        # Main game loop
└── README.md      # This file
```

## AI Algorithm

The AI uses **Minimax with Alpha-Beta Pruning**:
- **Easy**: depth 2, makes random valid moves sometimes
- **Medium**: depth 4, evaluates board positions
- **Hard**: depth 6, near-unbeatable with full board evaluation

The evaluation function scores based on:
- Center column control
- Horizontal, vertical, and diagonal window analysis
- Offensive and defensive move scoring

## Built With

- **Python 3**
- **Pygame CE** (Community Edition)
- **NumPy** (for sound generation)

## Author

Built as part of **InternPe** internship task.
