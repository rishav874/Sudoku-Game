# Sudoku-Game

# Overview of the Game
In this Sudoku game, the player interacts with a graphical user interface (GUI) to complete a pre-set grid. The game has a built-in feature to validate the correctness of the player's inputs. Additionally, it includes a solver function that can automatically solve the puzzle, highlighting the process step-by-step.

# Key Features
Graphical User Interface: A 9x9 grid is displayed, representing the Sudoku board. Each cell can either contain a pre-filled number or be empty for user input.
Number Entry: The user can select a cell and input numbers using the keyboard. The game checks the validity of each input.
Real-time Feedback: The game highlights the current cell, and error messages appear if the user enters an invalid number.
Sudoku Solver: A built-in backtracking algorithm can solve the puzzle automatically, providing step-by-step visual updates.
Restart and Default Grid: The user can reset the grid or reload the default puzzle at any point.

# Tools and Technologies Used
# Libraries Used:
Pygame:
1. pygame.display.set_mode(): Creates the game window of specified dimensions (500x500 in this case).
2. pygame.display.set_caption(): Sets the title of the game window.
3. pygame.font.SysFont(): Loads a system font (e.g., "comicsans") for rendering text on the screen.
4. pygame.event.get(): Captures events such as mouse clicks, key presses, and window closing.
5. pygame.draw.line(): Draws lines on the game window to create the Sudoku grid and highlight selected cells.
6. pygame.draw.rect(): Fills the Sudoku cells with a color to highlight pre-filled numbers.
7. pygame.mouse.get_pos(): Retrieves the current mouse position, allowing players to select cells by clicking.
8. pygame.key.get_pressed(): Detects key presses, letting the player input numbers.

# Functions Used:
1. cord(pos):
Converts the mouse click position into grid coordinates (row and column).
Updates the global variables x and z, representing the current cell's row and column.

2. highlightbox():
Draws a highlighted box around the currently selected cell using thick lines.
Helps the player see which cell is currently active.

3. drawlines():
Draws the grid lines for the Sudoku board.
Differentiates major grid sections (3x3 sub-grids) by making the lines thicker.

4. fillvalue(value):
Displays a number (entered by the player) in the currently selected cell.

5. raiseerror() / raiseerror1():
Displays an error message if the player attempts to input an invalid number or key.

6. validvalue(m, k, l, value):
Checks if the input number (value) is valid for the selected cell (ensuring no conflicts with other numbers in the same row, column, or 3x3 sub-grid).

7. solvegame(defaultgrid, i, j):
Solves the Sudoku puzzle using backtracking.
The function iteratively tries filling empty cells, checks for validity, and backtracks if necessary.

8. ngameresult():
Displays a "game finished" message when the puzzle is successfully solved.
