# N-Queens Problem Solution

## Overview
This repository contains a C++ solution to the **N-Queens** problem, a classic backtracking problem from LeetCode. The goal is to place N queens on an NxN chessboard such that no two queens threaten each other. This solution uses a backtracking approach to generate all possible configurations.

## Problem Description
The N-Queens problem requires placing N queens on an NxN chessboard such that:
- No two queens share the same row.
- No two queens share the same column.
- No two queens share the same diagonal.

Given an integer `n`, the program returns all distinct solutions to the N-Queens problem. Each solution is represented as a vector of strings, where:
- `'Q'` represents a queen.
- `'.'` represents an empty cell.



**Example for n = 4:**
```
[
 [".Q..",
  "...Q",
  "Q...",
  "..Q."],

 ["..Q.",
  "Q...",
  "...Q",
  ".Q.."]
]
```

## Approach
The solution uses a **backtracking** algorithm with the following steps:
1. **Board Initialization**: Create an NxN board filled with `'.'` characters.
2. **Safety Check**: For each position `(row, col)`, check if it's safe to place a queen by verifying:
   - No queen in the same row.
   - No queen in the same column.
   - No queen in the left or right diagonals.
3. **Recursive Placement**:
   - Place a queen in a safe column of the current row.
   - Recursively attempt to place queens in the next row.
   - If a solution is found (all queens placed), add it to the result.
   - Backtrack by removing the queen and trying the next column.
4. **Result Collection**: Store all valid board configurations in a vector.

**Time Complexity**: O(N!), as it explores all possible queen placements.
**Space Complexity**: O(N²) for the board and recursion stack.


## File Structure
```
N-Queens/
├── N_Queens.cpp  # C++ solution for the N-Queens problem
├── README.md     # This file
```

## Setup and Compilation
To run the program, follow these steps:

1. **Clone the Repository**:
   ```
   git clone https://github.com/Sanju-1114/N-queens.git
   ```

2. **Compile the Code**:
   Use a C++ compiler like `g++`:
   ```
   g++ N_Queens.cpp -o nqueens
   ```

3. **Run the Program**:
   Execute the compiled binary:
   ```
   ./nqueens
   ```

4. **Modify Input**:
   The default board size is `n = 4`. To change it, modify the `n` variable in the `main()` function of `N_Queens.cpp`.

**Requirements**:
- C++ compiler (e.g., g++ with C++11 or later).
- Standard libraries: `<iostream>`, `<vector>`, `<string>`.

## Example Output
For `n = 4`, the program outputs all valid configurations:
```
.Q..
...Q
Q...
..Q.

..Q.
Q...
...Q
.Q..
```


Each configuration is printed as an NxN grid, with a blank line separating solutions.

This is very important question to understand the backtracking.


## Usage
- **For Learning**: Study the `isSafe` and `nQueens` functions to understand backtracking and board validation.
- **For Interviews**: The code is optimized for clarity and efficiency, making it a good reference for coding interviews.
- **For Extension**: Modify the code to visualize the board or count solutions instead of printing them.

## Contributing
Feel free to fork this repository and submit pull requests with improvements, such as:
- Adding visualizations for the board.
- Optimizing the backtracking algorithm.
- Supporting additional input formats.


## Contact
For questions or suggestions, reach out via [GitHub Issues](https://github.com/Sanju-1114/N-queens/issues).
