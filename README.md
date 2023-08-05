# Sudoku Solver with API Integration

This project is a Sudoku Solver web application that allows users to pull from API a Sudoku puzzle and then solve it using a backtracking algorithm. The application utilizes HTML, CSS, and JavaScript to create an interactive and user-friendly interface. The Sudoku puzzle is pulled from an external API, making it easy for users to get puzzles to solve.

## Features

- Sudoku puzzle generation from an external API.
- Solving the puzzle using a backtracking algorithm.
- Interactive and responsive user interface.


## How to Use

1. Clone the repository to your local machine.
2. Open the `index.html` file in your web browser.
3. Click "GetPuzzle" button, application will fetch a Sudoku puzzle from the API automatically.
4. To solve the puzzle, click on the "SolvePuzzle" button, and the solution will be displayed.


## Technologies Used

- HTML
- CSS
- JavaScript (Vanilla JS)

## How the Sudoku Solver Works

The Sudoku Solver in this project is implemented using a backtracking algorithm, which is a common method for solving Sudoku puzzles. The algorithm works as follows:

1. Find an empty cell in the Sudoku grid. If no empty cell is found, the puzzle is solved.
2. Attempt to fill the empty cell with a number from 1 to 9.
3. Check if the number is valid in the current cell according to the Sudoku rules (no repetition of the same number in the row, column, or 3x3 subgrid).
4. If the number is valid, move to the next empty cell and repeat steps 1 to 3 recursively.
5. If the number is not valid, backtrack by changing the number in the current cell and try a different number.
6. Continue the process until a valid solution is found or all possibilities are exhausted.

## External API

The Sudoku puzzle is fetched from an external API that provides random Sudoku puzzles for solving. The API returns a 2-dimensional array representing the 9x9 Sudoku grid. The empty cells are represented by the number 0.

API Endpoint: `https://sugoku.onrender.com/board?difficulty=easy`

Sample API Response:

```json
{
  "puzzle": [
    [5, 3, 0, 0, 7, 0, 0, 0, 0],
    [6, 0, 0, 1, 9, 5, 0, 0, 0],
    [0, 9, 8, 0, 0, 0, 0, 6, 0],
    [8, 0, 0, 0, 6, 0, 0, 0, 3],
    [4, 0, 0, 8, 0, 3, 0, 0, 1],
    [7, 0, 0, 0, 2, 0, 0, 0, 6],
    [0, 6, 0, 0, 0, 0, 2, 8, 0],
    [0, 0, 0, 4, 1, 9, 0, 0, 5],
    [0, 0, 0, 0, 8, 0, 0, 7, 9]
  ]
}
```

![Capture1](https://github.com/brhmpreet/Sudoku-Solver/assets/97327612/0039be2c-96db-4d3d-8a2b-e196f667ef36)
![Capture2](https://github.com/brhmpreet/Sudoku-Solver/assets/97327612/e6c2e8b5-dcab-45cc-92ee-f678dedbdf3a)

## Acknowledgments

- Thanks to the developers of the external API for providing Sudoku puzzles.
- The backtracking algorithm implementation is inspired by various online resources and tutorials.
