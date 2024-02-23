# Backtracking 

> Backtracking is an algorithmic technique where the goal is to get all solutions to a problem using the brute force approach. It consists of building a set of all the solutions incrementally. Since a problem would have constraints, the solutions that fail to satisfy them will be removed.

An example of backtracking usage is in solving Sudoku puzzle (there are other examples in this repo that use backtracking as well). 
To find the right value for a position in a sudoku puzzel you choose one of the possibilities and check if you can solve the next position. This recursion will help trying all possible solutions, since if a solution fail we go back one step and try rest of the possibilities, and we do this till a possibility that is a solution will be tried.

Check this C snippet for solving a 9x9 Sudoku board (from https://github.com/sepgh/remember-c-dummy-practices/blob/main/sudoku/app.c):

```c
bool solve(Sudoku* sudoku, int index){
    int row = floor(index / 9);
    int col = floor(index % 9);


    if (index == (9*9))
        return true;
    if (sudoku->board[row][col] != 0){
        return solve(sudoku, index + 1);
    }

    
    int possible_numbers[] = {1,2,3,4,5,6,7,8,9};
    
    // Checking horizontal
    int z;
    for(z = 0; z < 9; z++){
        int val = sudoku->board[row][z];
        if (val == 0){
            continue;
        }
        possible_numbers[val-1] = 0;
    }

    // Checking vertical
    for(z = 0; z < 9; z++){
        int val = sudoku->board[z][col];
        if (val == 0){
            continue;
        }
        possible_numbers[val-1] = 0;
    }


    // Checking inner box
    int box_first_row = floor(row / 3) * 3;
    int box_first_col = floor(col / 3) * 3;

    // printf("Box > ");

    int m,n;
    for (m = 0; m < 3; m++){
        for (n = 0; n < 3; n++){
            int val = sudoku->board[box_first_row+m][box_first_col+n];
            if (val == 0){
                continue;
            }
            possible_numbers[val-1] = 0;
        }            
    }

    // BACKTRACKING
    bool solved_index = false;
    for (int si = 0; si < 9; si++){
        if (possible_numbers[si] != 0){
            sudoku->board[row][col] = possible_numbers[si];
            if (solve(sudoku, index+1)){
                solved_index = true;
                break;
            }
        }
    }

    if (!solved_index){
        sudoku->board[row][col] = 0;
    }
    return solved_index;
}
```

