# Tic-Tac-Toe-Game-Saanvi-Awasthi
# Tic-Tac-Toe Game 🎮

A classic two-player Tic-Tac-Toe game implemented in Python for the command line.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Instructions for testing](#testing#)
- [How to Play](#how-to-play)
- [Game Rules](#game-rules)
- [Code Structure](#code-structure)
- [Example Gameplay](#example-gameplay)
- [Troubleshooting](#troubleshooting)
- [Future Enhancements](#future-enhancements)
- [License](#license)

## 🎯 Overview

This is a simple, interactive command-line implementation of the classic Tic-Tac-Toe game (also known as Noughts and Crosses). Two players take turns placing their marks (X and O) on a 3x3 grid, with the goal of getting three marks in a row horizontally, vertically, or diagonally.

## ✨ Features

- **Two-Player Gameplay**: Play against a friend locally
- **Input Validation**: Robust error checking for all user inputs
- **Clear Board Display**: Visual grid with coordinate labels
- **Win Detection**: Automatically detects winning combinations
- **Draw Detection**: Recognizes when the game ends in a tie
- **User-Friendly Messages**: Clear prompts and feedback throughout the game
- **Simple Interface**: Easy-to-understand coordinate system (0-2 for rows and columns)

## 🔧 Requirements

- Python 3.6 or higher
- No external dependencies required (uses only Python standard library)

## 📥 Installation

1. **Download the game file**:
   ```bash
   # Save the code as tictactoe.py
   ```

2. **Verify Python installation**:
   ```bash
   python --version
   # or
   python3 --version
   ```

3. **No additional packages needed** - the game uses only built-in Python modules!
## INSTRUCTIONS FOR TESTING: • When prompted, enter your moves by specifying row and column numbers separated by a space (e.g., 1 2). • Only positions labelled with a blank space can be chosen. • The game validates each move and will prompt again if the input is invalid. • After a win or draw, the game exits automatically.

## 🎮 How to Play

1. **Start the game**:
   ```bash
   python tictactoe.py
   # or
   python3 tictactoe.py
   ```

2. **Enter your moves**:
   - When prompted, enter the row and column numbers separated by a space
   - Format: `row col` (e.g., `1 1` for the center cell)
   - Both row and column must be 0, 1, or 2

3. **Take turns**:
   - Player X goes first
   - Players alternate turns until someone wins or the board is full

4. **Win or Draw**:
   - Get three marks in a row (horizontal, vertical, or diagonal) to win
   - If all cells are filled with no winner, the game ends in a draw

## 📖 Game Rules

### Objective
Be the first player to get three of your marks in a row (horizontally, vertically, or diagonally).

### Board Coordinates
```
   0   1   2
0    |   |  
   ---|---|---
1    |   |  
   ---|---|---
2    |   |  
```

### Valid Moves
- Row number: 0, 1, or 2
- Column number: 0, 1, or 2
- The selected cell must be empty

### Winning Conditions
- **Horizontal**: Three marks in any row
- **Vertical**: Three marks in any column
- **Diagonal**: Three marks from corner to corner

### Examples of Winning Positions
```
X | X | X     X | O | O     X | O |      | O | X
  |   |         | X |         | X | O    | X | O
  |   |         |   | X     O |   | X  X | O |  
```

## 🏗️ Code Structure

### Functions

**`create_board()`**
- Creates and returns a new 3x3 game board
- Returns: 2D list filled with empty spaces

**`print_board(board)`**
- Displays the current state of the board
- Parameters: `board` - the game board to display

**`check_win(board, player)`**
- Checks if the specified player has won
- Parameters: 
  - `board` - current game state
  - `player` - 'X' or 'O'
- Returns: `True` if player has won, `False` otherwise

**`check_draw(board)`**
- Checks if the game has ended in a draw
- Parameters: `board` - current game state
- Returns: `True` if board is full, `False` otherwise

**`get_player_input(player, board)`**
- Gets and validates player move input
- Parameters:
  - `player` - current player ('X' or 'O')
  - `board` - current game state
- Returns: tuple of (row, col) coordinates

**`play_game()`**
- Main game loop that orchestrates the entire game
- Manages turn switching and game state

## 💡 Example Gameplay

```
--- Welcome to Tic-Tac-Toe! ---

   0   1   2
0    |   |  
   ---|---|---
1    |   |  
   ---|---|---
2    |   |  

Player 'X', enter move (row col): 1 1

   0   1   2
0    |   |  
   ---|---|---
1    | X |  
   ---|---|---
2    |   |  

Player 'O', enter move (row col): 0 0

   0   1   2
0  O |   |  
   ---|---|---
1    | X |  
   ---|---|---
2    |   |  

Player 'X', enter move (row col): 0 1
...
```

## 🔍 Troubleshooting

### Common Issues

**Problem**: "Invalid input" error
- **Solution**: Make sure you enter TWO numbers separated by a space (e.g., `1 2`, not `1,2` or `12`)

**Problem**: "Coordinates out of range" error
- **Solution**: Both numbers must be 0, 1, or 2

**Problem**: "That cell is already taken" error
- **Solution**: Choose a different empty cell

**Problem**: Game doesn't start
- **Solution**: Ensure you have Python 3.6+ installed and run the file from the command line

## 🚀 Future Enhancements

Potential improvements for future versions:

1. **Single Player Mode**: Add AI opponent with difficulty levels
2. **Score Tracking**: Keep track of wins across multiple games
3. **Replay Option**: Allow players to start a new game without restarting
4. **Custom Board Size**: Support for larger grids (4x4, 5x5)
5. **Colorful Display**: Add ANSI color codes for better visualization
6. **Move History**: Display list of previous moves
7. **Undo Feature**: Allow players to take back their last move
8. **Save/Load Gam<img width="1920" height="1080" alt="Screenshot 2025-11-23 152842" src="https://github.com/user-attachments/assets/000acb9e-6690-4e38-a70a-8e29cc2f290d" />
<img width="1920" height="1080" alt="Screenshot 2025-11-23 152851" src="https://github.com/user-attachments/assets/07d11630-b1a3-47e8-b3ca-4fc02dd38467" />
<img width="1920" height="1080" alt="Screenshot 2025-11-23 152858" src="https://github.com/user-attachments/assets/26263bcb-053d-4a50-8e93-b0c53b567055" />
