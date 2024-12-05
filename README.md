# **Tic-Tac-Toe Game**
A simple text-based Tic-Tac-Toe game implemented in Python. This project basically highlights features such as loops, conditions, functions, and modularity that are basic in programming with the extra touch of a graphical user interface to show a true representation of the game, which can be played by two players at a go.

________________________________________
## **Features**
Interactive Gameplay: Two players turn by turn place their marks ‘X’ or ‘O’ on a 3x3 board or a 3x3 cardboard having nine compartments.
Input Validation: Eases the possibilities of a player to choose only genuine and unoccupied cell.
Win/Tie Detection: Identifies win condition such as rows, columns or diagonals, or draws when all the areas of the board are filled.
Error Handling: Retrieves and reports invalid inputs within the app without causing system fail and gives appropriate error messages.
Clean and Modular Code: It is important for functions to be optimized, so that reading through the code is not a tedious cumbersome task.

________________________________________
## **How to Play**
1.	Run the program in your Python environment.
2.	The game will display a 3x3 grid representing the board.
3.	Players take turns entering a number (1-9) corresponding to the desired cell:
o	1 is the top-left cell, 9 is the bottom-right cell.
4.	The game will announce the winner or declare a tie when all cells are filled.
   
________________________________________
# **Game Controls**
| Number | Cell Position   |
|--------|-----------------|
| 1      | Top-Left        |
| 2      | Top-Middle      |
| 3      | Top-Right       |
| 4      | Middle-Left     |
| 5      | Center          |
| 6      | Middle-Right    |
| 7      | Bottom-Left     |
| 8      | Bottom-Middle   |
| 9      | Bottom-Right    |

________________________________________
# **How to Run**
**Prerequisites**
•	Python 3.x installed on your system.
**Steps**
1.	Clone the repository:
git clone [https://github.com/avikashetty/Tictactoe]
2.	Navigate to the project directory:
cd Tictactoe
3.	Run the program:
python tictactoe.py

________________________________________
# **Project Structure**
•	tictactoe.py: The main Python file containing the game logic and functionality.
•	README.md: Documentation for the project, including setup instructions and gameplay details.

________________________________________
# **Code Highlights**
**1.	Game Board Initialization:**
board = [[" " for _ in range(3)] for _ in range(3)]
**2.	Win Detection:**
def check_winner(board, player):
    for row in board:
        if all(cell == player for cell in row):
            return True
    for col in range(3):
        if all(board[row][col] == player for row in range(3)):
            return True
    if all(board[i][i] == player for i in range(3)) or all(board[i][2 - i] == player for i in range(3)):
        return True
    return False
**3.	Player Input Validation:**
def get_player_input(board, player):
    while True:
        try:
            move = int(input(f"Player {player}, enter your move (1-9): ")) - 1
            row, col = divmod(move, 3)
            if 0 <= move <= 8 and board[row][col] == " ":
                return row, col
            else:
                print("Invalid move. Try again.")
        except ValueError:
            print("Please enter a valid number.")
  	
________________________________________
# **Future Improvements**
•	AI Opponent: Implement a computer player with strategic moves using the minimax algorithm.
•	Graphical Interface: Build a GUI version of the game using Tkinter or PyGame.
•	Online Multiplayer: Add networking capabilities to allow players to compete remotely.
________________________________________

# **Acknowledgements**
•	Python documentation for its excellent resources.
•	Various online tutorials and guides that provided inspiration and best practices.
________________________________________

# **License**
This project is open-source and available under the MIT License.

