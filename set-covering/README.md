# Set Covering Problem

The Set Covering Problem is a well-known problem in which you have some subsets of a universal set. The goal is to find the least number of subsets which covers the universal set.

We revisited the problem in this way:
- we have a main line of missing tiles and a certain number of lines containing some of them;
- the goal is to find a set of lines of tiles which cover all the main line.

Graphically:
- Main line: 
    >--------: (imagine that these tiles are missing 🙃)
- Set of lines:
    >-- - -- -:

    >-- -- - -:

    >---  - ---:

## Code

The code found in this directory is a readjustment of the lecture available [here](https://github.com/squillero/computational-intelligence/blob/master/2023-24/set-covering.ipynb). 

I extended the content, reorganized the code and created new functions implementing the following algorithms:
- Breadth-First search;
- Depth-First search;
- Uniform-Cost search;
- Greedy Best-First search;
- Depth-Limited search;
- Iterative-Deepening search.