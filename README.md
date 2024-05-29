# Minesweeper AI

## Overview

This project implements a Minesweeper game with an AI agent capable of playing the game. The game features a graphical interface for user interactions and AI-based moves.

## Repository Structure

```plaintext
.
├── runner.py               # Main file to run the Minesweeper game with GUI
├── core/
│   └── minesweeper.py      # Core logic for Minesweeper and AI
└── assets/
    ├── fonts/              # Fonts for the GUI
    └── images/             # Images for mines and flags
```

## Game Description

Minesweeper is a puzzle game where the objective is to clear a board containing hidden mines without detonating them, using clues about the number of neighboring mines.

## Running the Project

### Install
Ensure you have `pygame` installed. You can install it via pip:

```sh
pip install -r requirements.txt
```

### Run
To run the Minesweeper game, execute the `runner.py` file:

```sh
python runner.py
```

Ensure the necessary assets are in the `assets` directory.

## Algorithm Explanation

The AI uses logical inference to deduce safe cells and mines:

1. **Initial Setup**: The board is initialized, and mines are placed randomly.
2. **User Move**: The user clicks a cell. If it’s a mine, the game is lost. Otherwise, the number of nearby mines is revealed.
3. **AI Knowledge Update**: The AI updates its knowledge base with the new information from the user's move.
4. **Inference**: The AI infers new safe cells and mines from its knowledge base:
    - If a sentence’s mine count equals the number of cells, all cells are mines.
    - If a sentence’s mine count is zero, all cells are safe.
5. **Safe Move**: The AI makes a move on a known safe cell. If no safe cell is known, it makes a random move with the lowest mine probability.
6. **Repeat**: Steps 2 to 5 repeat until all mines are flagged or a mine is hit.

## Contact

For questions or contributions, contact via Telegram: [Sepehr0Day](https://t.me/Sepehr0Day).
