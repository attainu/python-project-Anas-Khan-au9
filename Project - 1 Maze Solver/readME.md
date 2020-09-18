             MAZE SOLVER
         ````````````````````
         ````````````````````

> Project Description
> Instructions to execute the file

    PROJECT DISCRIPTION:
    ____________________

Objectives:-
````````````
->  A maze in the form of a matrix will be given in the form of 1's and 0's, where
    1 represents the open path and 0 represents the blocked path.

->  And the goal is to find the path between the source to the destination in the 
    maze otherwise just return /"-1" indicating no path found.

Concepts used:-
```````````````

*   Backtracking

*   File handling


Approach:-
``````````

->  Given an maze, NxN matrix. We have to find a path from source to destination.
->  Maze [0][0] (top left corner) is the source and maze [N-1][N-1] (bottom right corner) is the destination.
->  There are few cells which are blocked, means we cannot enter into those cells. We can move in any direction
    (left, right, upa nd down).


* Create a solution matrix of the same structure as maze.
* Whenever we move to cell in a maze, mark that perticular cell in solution matrix.
* At the end print the solution matrix, follow that 1's from top corner, it will be the path.

Implementation/Algorithms:-
````````````````````````````
* If we reach at the destination - print the solution matrix.

*Else - ~mark the current cell in solution matrix as 1.
        
        
> If previous step is not in vertical direction (upwards) then move foreward in the vertical 
  direction (downwards) and recursively check if this movement leads to solution.

> If movement in above step doesn't lead to the solution and if previous step is not in horizontal 
  direction(left) then move forward in the horizontal direction (right) and recursively check if 
  this movement leads to the solution.

> If movement in above step doesn't lead to the solution and if privious step is not in 
  vertical direction (downwards) then move forward in the horizontal direction (upwards) and 
  recursively check if this movement leads to solution.

> If movement in above step doesn't lead to the solution and if privious step is not in 
  horizontal direction (towards right) then move forward in the horizontal direction (towards left) and 
  recursively check if this movement leads to solution.

> If one of the above solution works then backtrack and mark the current cell as 0.

NOTE: It is important to check the previous direction in which we have moved because if we will 
      move in opposite direction w.r.t. its previous direction might end up in infinite loop.



Taking Input:-
``````````````

* Open a file, say inputfile.txt, in write mode.
* Take the input for the order of the input matrix.
* Close the file.
* Again open the input.txt file in append mode.
* Take the input Matrix/maze in the form of NxN, close the inputfile.txt.
* Open the file inputfile.txt in read mode.

OUTPUT:-
`````````

* Open a file, say outputfile.txt, in write mode.

Instructions to Execute he file:-
__________________________________

*Open : https://github.com/attainu/python-project-Anas-Khan-au9

* From github repo copy the code of the file ta any python editor and save the file in
  a certain folder.

*Open and go to the folder where you save the python code.

*Execute the code file by writing - mazesolver.py or mazesolver.py -i inputfile.txt -o outputfile.txt

*Pass the argument in the following order.

*Give size of matrix = n

*n (any integer)

* 10100..1 (n binary digits with space seperated)

* Type n rows as above.


Sample input-:
"""
"copy paste" D:\WORK\Project - 1 Maze Solver>

5 (size of matrix)

"""
1 1 1 1 1

1 0 1 0 1

1 0 0 1 1

1 1 0 1 0 

1 0 0 1 1

"""

* The output will be printed in outputfile.txt and not on the terminal.


Sample output in outputfile.txt-:

1 0 0 0 0

1 0 0 0 0

1 0 0 0 0

1 0 0 0 0

1 1 1 1 1 

And input matrix will display in the "inputfile.txt"



