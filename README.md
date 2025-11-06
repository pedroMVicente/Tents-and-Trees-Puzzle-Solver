🏕️ Logic Programming Project
A “Tents and Trees” Puzzle Solver in Prolog

📘 Project Overview

This project was developed as part of the Logic for Programming course (2023–2024).
The goal is to implement a solver for the well-known logic puzzle “Tents and Trees” using Prolog.

In this puzzle, the objective is to place a tent next to each tree on a grid while following these rules:

Each tree must be associated with exactly one tent.

No two tents can touch each other — not even diagonally.

The number of tents in each row and column must match the provided clues.

The program uses logical reasoning and constraint solving to automatically find valid solutions to the puzzles.

⚙️ Features

Representation of puzzles using lists of lists (matrix structure).

Query predicates to access and analyze puzzle data (e.g., neighbors, empty cells).

Functions to insert tents and grass into the board.

Implementation of different solving strategies:

Filling complete rows/columns with grass.

Marking inaccessible cells.

Automatically placing tents when only one valid position exists.

Cleaning tent surroundings (no adjacent tents).

A backtracking-based solver to explore possible solutions when logic alone isn’t enough.

🧩 Implemented Predicates

Some of the main predicates implemented include:

vizinhanca/2 and vizinhancaAlargada/2 – determine neighboring cells.

todasCelulas/2,3 – list all coordinates or cells containing a specific object.

celulaVazia/2 – checks if a cell is empty or grass.

insereObjectoCelula/3, insereObjectoEntrePosicoes/4 – insert tents or grass.

relva/1, inacessiveis/1, aproveita/1, unicaHipotese/1, limpaVizinhancas/1 – apply solving strategies.

valida/2 – ensures a one-to-one relation between trees and tents.

resolve/1 – attempts to solve the puzzle completely.

🧠 Technologies Used

Language: Prolog (SWI-Prolog recommended)

Libraries: clpfd for constraint logic programming

🗂️ Project Structure

project/
│
├── puzzlesAcampar.pl      # Provided puzzle definitions
├── projectoLP_Acampar.pdf # Project description (this document)
└── main.pl                # Your main Prolog implementation file

🚀 How to Run

1) Open the project in SWI-Prolog.

2) Load your main file:
  ?- [main].

3) Load a sample puzzle:
  ?- puzzle(6-14, P).

4) Solve it:
   ?- resolve(P).

🧑‍💻 Author

Pedro Vicente
Logic for Programming — 2023/2024

