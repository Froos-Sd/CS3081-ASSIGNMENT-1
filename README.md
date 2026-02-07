# Tic-Tac-Toe

Name: Firas Saadeddin
Student ID: S23208870
Course: CS3081 – Artificial Intelligence
Instructor: Dr. Naila Marir
Semester: Spring 2026

 Project Description

This project implements an unbeatable Tic-Tac-Toe AI using the Minimax algorithm.
The AI plays optimally against a human player, meaning the best possible outcome for the human is a tie.

The graphical interface is provided using pygame, while all game logic and AI decision-making are implemented in tictactoe.py.

 Implementation Approach

The game board is represented as a 3×3 list, where each cell can contain:

"X" for player X

"O" for player O

None for an empty cell

The AI logic is built by implementing the following core functions:

player(board) – Determines whose turn it is

actions(board) – Returns all possible valid moves

result(board, action) – Returns a new board after applying a move

winner(board) – Checks if X or O has won

terminal(board) – Checks if the game is over

utility(board) – Assigns a score to terminal states

minimax(board) – Selects the optimal move

Player X is treated as the maximizing player, while O is the minimizing player.
The Minimax algorithm recursively explores all possible game states and selects the move that leads to the best guaranteed outcome.

 Bonus: Alpha–Beta Pruning

To improve efficiency, Alpha–Beta Pruning was implemented as an optimization to the Minimax algorithm.

Alpha–Beta Pruning reduces the number of game states evaluated by eliminating branches that cannot affect the final decision.
It uses two values:

Alpha (α): the best value the maximizing player can guarantee

Beta (β): the best value the minimizing player can guarantee

When alpha ≥ beta, further exploration of that branch is stopped (pruned).
This optimization makes the AI faster while producing the same optimal results.

 Challenges Faced

One of the main challenges was:

Ensuring that the original board state was never modified during Minimax recursion

This was solved by using deep copies of the board when generating new game states.
Another challenge was understanding the recursive nature of Minimax and correctly switching between maximizing and minimizing players.







