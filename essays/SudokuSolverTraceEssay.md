---
layout: essay
type: essay
title: Backtracking Sudoku Solver 
date: 2015-08-26
labels:
  - Software Engineering
  - Learning
---

Backtracking Sudoku Solver 
Joe Palma
The number of solutions for a cell in a sudoku puzzle is based off the legal values for that cell. In a backtracking algorithm it test every legal value for a cell recursively, searching to find if the legal value satisfies a solution for the puzzle based off the next cell. Because of this the algorithm could go many levels deep in its layers of solutions before it discovers that a legal value many cells back isn�t a solution. The code would then start over at the cell where the issue arose. 
The solving time for puzzles 3 and 4 takes longer for the backtracking style sudoku solver algorithm because those puzzles have a higher number of solutions. Each time the solveSudoku method test a legal value it receives if there is a solution for that value or not, if there are a large number of legal values possible for each cell, then the backtracking step of the algorithm will take a very long time because it needs to test each value. It could find a solution for a string of legal values, but if it has to backtrack and test a large array for every time a legal value isn�t a solution it is going to take a long time to finish for puzzles with many possible solutions. Each element in a string of solutions can add an exponential amount of runtime to the overall runtime of the program. 
To optimize this you can implement constraint satisfaction to test if a given legal value satisfy the constraints set by preceding legal values. If the solver finds a solution for a given legal value within the constraints of prior legal values vs the looser constraint of being a solution for the entire puzzle the algorithm would backtrack less and find a solution faster. 