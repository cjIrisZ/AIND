# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Naked twins refers to two positions A and B in the same unit(row, col, square, or might include diagonal) of the Sudoku, that both have the same possibilities of two, num1 and num2. Position A and B can only be num1 or num2, so these two posibilities must go in these two positions, no other alternatives for these two positions. Thus, in the same unit, we can exlude other positions with these two posibilities, in other words, positions with posibilities of num1 and num2 can be eliminated.
In the python script, it iterates through all units of the Sudoku, and checks if there are naked twins using dictionary. The dictionary store the 2-digit possibilities as key, and positions as value. If the key already exists, means there are naked twins. If there are naked twins, iterates in the unit, and eliminates the possibilities in other positions.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The easiest way to incorporate diagonal contraint was to include it as an additional unit in sudoku. Then, the diagonal entries will have corresponding diagonal entries as their peers. So that the script will eliminate the possibilities that already confirmed in other positions. And solutions that do not satisfy the diagonal constraint will not be accepted.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

