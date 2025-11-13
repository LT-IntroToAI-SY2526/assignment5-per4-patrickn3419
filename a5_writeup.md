# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. What are some things that you learned through this assignment? Think about the concepts of backtracking, constraint satisfaction, and search algorithms. Were there any particular challenges you faced while implementing the Board class methods or the DFS/BFS functions? How did you overcome them?

I learned about how different search functions have different types of classes to define the route they take to find the solution. I now understand the concept of backtracking when the program runs into a failure condition so it can stop going down a route. Some problems I faced while implementing the Board class methods was that it was sometimes hard to keep track of the functions and classes that have already been defined an use them instead of trying to make something from scratch. This was an easy fix since when I explored all of the code that was already given to me I had an understanding for the backbone of the code.



2. How can you apply what you learned in this assignment to future programs or projects? Consider other types of problems that involve searching through possibilities, making decisions, and backtracking when those decisions don't work out. Can you think of real-world scenarios where DFS or BFS might be useful? What about other constraint satisfaction problems?

I can apply the search functions I learned about in this assignment to other programs or projects which may require finding solutions when using a simple function isn't enough. Real-world scenarios where DFS or BFS might be useful may be scheduling timeslots fo events where we can't have two events happening at the same time. It could also be useful in dealing with large mathmatical problems where it may take more than one step to get to a solution, such as in algebra or trig.



3. Explain how the Stack and Queue classes work and why they are important for DFS and BFS algorithms. Describe the difference between LIFO (Last In First Out) and FIFO (First In First Out) data structures. How does using a Stack versus a Queue change the way the search algorithm explores possible solutions? Why is one data structure better suited for depth-first search and the other for breadth-first search?

The breadth first search (BFS) method uses the Queue class, which would be a FIFO (first in first out) data structure. The queue class allows for elements to be pushed, and then for the oldest element to be popped out. This allows for the program to go through all of the iterations of an earlier fork rather than diving in all the way into a specific iteration when we push and pop copies of the game board. On the other hand, the depth first search (DFS) method uses the Stack class, which has a LIFO (last in first out) data structure. The Stack class allows for elements to be pushed, similarly to the Queue class, but instead pops out the most recent element that was added. This means that when we make a copy of the board to perform iterations on, the program will keep popping out the board with the most recent progress, and keep working on that iteration until it runs into an error. This is different from the Queue class, which pops out the oldest copy of the board and works on all the iterations at once. 

Based on the methods the two search functions use, BFS would be optimal for finding the solution the quickest when there aren't many routes to go down (meaning that the solution is short/shallow), and DFS would be better at finding one very specific solution that is very deep. DFS can explore deep trees of iterations efficiently while BFS thouroughly explores every possible iteration before reaching the solution. This also means that BFS is less memory efficient than DFS, because it has to store many more interations.