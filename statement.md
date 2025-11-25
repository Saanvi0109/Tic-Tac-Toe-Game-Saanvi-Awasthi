### POBLEM STATEMENT: The challenge is to implement a two-player Tic-Tac-Toe game on a 3x3 grid played in turns. Players alternate moves, placing 'X' or 'O' in empty cells. The objective is to connect three of their symbols in a straight line—horizontally, vertically, or diagonally—before the opponent does. If the grid is filled without any player achieving this, the game is declared a draw.

### SCOPE OF THE PROJECT: 
1)Console-based game for 2 participants using text input/output.

2)Handles all aspects of gameplay: board creation, move validation, alternate turns, win/draw detection, and display of current state.

3)Enforces game rules strictly (valid moves, switching turns, preventing overwriting).

4)Provides clear victory and draw announcements.

5)Optional extensions (not in current scope):

6)Support for larger grids or custom win lengths.

7)Automated or AI players.

8)Graphical user interface.

### TARGET USERS: 1)Python learners and beginners looking to practice logic, data structures, and input/output operations.

2)Anyone wanting to play a quick terminal Tic-Tac-Toe game.

3)Students and educators demonstrating turn-based game logic.

HIGH-LEVEL FEATURES: 1)Game Initialization: Sets up an empty board, ensures clear display with row/column indices.​

2)Move Input and Validation: Prompts user input for moves and validates proper format, boundaries, and empty cell requirement.

3)Turn Management: Alternates turns between Player 'X' and Player 'O'.

4)Win Detection: Checks rows, columns, and diagonals after every move for a victory condition.

5)Draw Detection: Recognizes full boards without a winner and declares a draw.

6)End-of-Game Announcements: States the result after each round.

7)Simple, robust structure: Each function handles an essential piece of game logic.
## Purpose
This project implements the classic Tic-Tac-Toe game as a command-line application, providing an interactive gaming experience for two players. The application demonstrates fundamental programming concepts including game logic, input validation, win condition checking, and user interaction through a simple, intuitive text-based interface.

#Project Objectives

### Primary Goals
1. Create a fully functional two-player Tic-Tac-Toe game
2. Implement robust input validation and error handling
3. Provide clear visual feedback through board display
4. Detect all win conditions and draw scenarios
5. Deliver a smooth, user-friendly gaming experience

### Educational Goals
- Demonstrate modular function design
- Practice 2D list manipulation in Python
- Implement game state management
- Apply conditional logic and loop structures
- Handle user input validation comprehensively

## Technical Specifications

### Game Mechanics

**Board Structure:**
- 3x3 grid represented as a 2D list
- Each cell can contain: ' ' (empty), 'X', or 'O'
- Zero-indexed coordinate system (0-2 for both rows and columns)

**Player System:**
- Two players: 'X' and 'O'
- Player X always starts first
- Players alternate turns after each valid move

**Win Conditions:**
- **Horizontal Win**: Three identical marks in any row
- **Vertical Win**: Three identical marks in any column
- **Diagonal Win**: Three identical marks on either diagonal
  - Main diagonal: positions (0,0), (1,1), (2,2)
  - Anti-diagonal: positions (0,2), (1,1), (2,0)

**Draw Condition:**
- All 9 cells are filled with no winner present

### Core Functions

#### 1. `create_board()`
**Purpose:** Initialize a new game board  
**Returns:** 3x3 2D list filled with empty spaces  
**Usage:** Called once at the start of each game

#### 2. `print_board(board)`
**Purpose:** Display the current state of the board  
**Parameters:**
- `board`: Current game board (2D list)

**Output Format:**
```
   0   1   2
0  X | O |  
   ---|---|---
1    | X |  
   ---|---|---
2  O |   | X
```

#Features:
- Column headers for easy reference
- Row numbers for coordinate identification
- Visual separators between cells
- Clean, readable layout

#### 3. `check_win(board, player)`
**Purpose:** Determine if specified player has won  
**Parameters:**
- `board`: Current game board
- `player`: Player to check ('X' or 'O')

**Algorithm:**
1. Check all three rows for horizontal wins
2. Check all three columns for vertical wins
3. Check main diagonal (top-left to bottom-right)
4. Check anti-diagonal (top-right to bottom-left)

**Returns:** Boolean (True if player has won)

#### 4. `check_draw(board)`
**Purpose:** Determine if the game is a draw  
**Parameters:**
- `board`: Current game board

**Logic:** Iterates through all cells; returns False if any empty cell found

**Returns:** Boolean (True if board is full)

#### 5. `get_player_input(player, board)`
**Purpose:** Get and validate player move  
**Parameters:**
- `player`: Current player ('X' or 'O')
- `board`: Current game board

**Validation Steps:**
1. Check input format (two space-separated values)
2. Verify both values are numeric
3. Confirm coordinates are within range (0-2)
4. Ensure selected cell is empty

**Error Messages:**
- Invalid format: "Invalid input. Please enter TWO numbers separated by a space."
- Non-numeric input: "Invalid input. Please enter NUMBERS for row and col."
- Out of range: "Coordinates out of range. Must be 0, 1, or 2."
- Cell occupied: "That cell is already taken! Try aga
