# Sudoku Solver using Constraint Satisfaction Problem (CSP)

This project is a Sudoku solver implemented in Java using the Constraint Satisfaction Problem (CSP) approach. It reads a Sudoku puzzle, applies CSP techniques to solve it, and verifies the solution.

## Features

- **CSP Techniques**: Utilizes techniques such as elimination, single possible number, only choice in row/column/box to solve the puzzle.
- **Efficient**: Designed to solve puzzles efficiently with performance statistics.
- **Modular Design**: Clear separation of different CSP techniques for better readability and maintainability.

## Technologies Used

- **Java**: The programming language used for the implementation.
- **Eclipse/IntelliJ**: Recommended IDEs for development.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) installed (version 8 or above).
- An IDE like Eclipse or IntelliJ IDEA is recommended for running the project.

### Installation

1. **Clone the Repository**

    ```sh
    git clone https://github.com/yourusername/sudoku-csp-solver.git
    cd sudoku-csp-solver
    ```

2. **Open the Project in Your IDE**

    Open the cloned project in your preferred IDE.

3. **Run the Project**

    Locate the `SudokuCSP.java` file and run it.

### Usage

1. **Define the Sudoku Puzzle**

    The Sudoku puzzle to be solved is defined in the `firstSudoku` 2D array in the `SudokuCSP.java` file. Modify this array to solve different Sudoku puzzles.

    ```java
    public static int[][] firstSudoku = {
        {5, 0, 1, 0, 0, 0, 6, 0, 4},
        {0, 9, 0, 3, 0, 6, 0, 5, 0},
        {0, 0, 0, 0, 9, 0, 0, 0, 0},
        {4, 0, 0, 0, 0, 0, 0, 0, 9},
        {0, 0, 0, 1, 0, 9, 0, 0, 0},
        {7, 0, 0, 0, 0, 0, 0, 0, 6},
        {0, 0, 0, 0, 2, 0, 0, 0, 0},
        {0, 8, 0, 5, 0, 7, 0, 6, 0},
        {1, 0, 3, 0, 0, 0, 7, 0, 2},
    };
    ```

2. **Run the Solver**

    Run the `SudokuCSP.java` file. The program will display the initial Sudoku puzzle, solve it, and then display the solved puzzle along with the time taken.

### Project Structure

- **Cell.java**: Defines the `Cell` class representing each cell in the Sudoku grid.
- **SudokuCSP.java**: Main class implementing the CSP solver.

### Example Output

```sh
---------------------------------------------
 5 0 1 0 0 0 6 0 4
 0 9 0 3 0 6 0 5 0
 0 0 0 0 9 0 0 0 0
 4 0 0 0 0 0 0 0 9
 0 0 0 1 0 9 0 0 0
 7 0 0 0 0 0 0 0 6
 0 0 0 0 2 0 0 0 0
 0 8 0 5 0 7 0 6 0
 1 0 3 0 0 0 7 0 2
---------------------------------------------

SUDOKU IS CORRECTLY SOLVED!!!
---------------------------------------------
 5 3 1 2 7 8 6 9 4
 2 9 4 3 1 6 8 5 7
 6 7 8 4 9 5 2 1 3
 4 2 6 7 5 1 3 8 9
 3 5 7 1 6 9 4 2 8
 7 1 9 8 4 2 5 3 6
 9 4 5 6 2 3 1 7 8
 8 8 2 5 3 7 9 6 1
 1 6 3 9 8 4 7 4 2
---------------------------------------------
Sudoku Solved in : 123 ms

