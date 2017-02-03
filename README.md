# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Each box is inclluded in multiple units, each unit consists of the row\column\3x3 squares neighborhoods. The naked twins adds a new constraint to minimize the number of possibilities prior to performing a full search. The constraint is implemented by:
1- checking each of the boxes containing two values and looking for duplicates within each unit
2- if a duplicate is found, remove the values from other boxes within the same unit.
For effeciency, the two values are added to a dictionary, and other values are compared to the dictionary.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Diagonal sudoku adds a new constraint to the regular constraints. To add the constraint, we add new units for diagonal and anti-diagonal. And since constraint propagation uses each of the units separately, the new constraints will be part of the constraint propagation.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.