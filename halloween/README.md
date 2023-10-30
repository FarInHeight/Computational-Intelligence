# Halloween Challenge

Given the **Set Covering Problem**, find the best solution using *Single-state methods* with the fewest calls to the fitness functions for:

* `num_points = [100, 1_000, 5_000]`
* `num_sets = num_points`
* `density = [.3, .7]` 

## Answer

The Halloween challenge has been accepted. To solve it, I'd reply with the following methods (with some modifications described for each algorithm, if any):
- **Random-Mutation Hill Climber**;
- **Steepest-Step Hill Climber**;
- **Steepest-Step Hill Climber with Replacement**;
- **Tabu Search**;
- **Simulated Annealing**.

## Best Results[^1]

- **Combination: NUM_POINTS=100, NUM_SETS=100, DENSITY=0.3**

    Algorithm: `tabu_search` \
    Fitness function: `fitness2` \
    Terminated after 7 iterations. \
    Terminated after 6 changes. \
    Number of evaluations: 696. \
    Goal reached? Yes \
    State cost: 6

- **Combination: NUM_POINTS=100, NUM_SETS=100, DENSITY=0.7**

    Algorithm: `tabu_search` \
    Fitness function: `fitness1` | `fitness2` \
    Terminated after 4 iterations. \
    Terminated after 3 changes. \
    Number of evaluations: 399. \
    Goal reached? Yes \
    State cost: 3

- **Combination: NUM_POINTS=1000, NUM_SETS=1000, DENSITY=0.3**

    Algorithm: `tabu_search` \
    Fitness function: `fitness2` \
    Terminated after 12 iterations. \
    Terminated after 11 changes. \
    Number of evaluations: 1210. \
    Goal reached? Yes \
    State cost: 11

- **Combination: NUM_POINTS=1000, NUM_SETS=1000, DENSITY=0.7**

    Algorithm: `tabu_search` \
    Fitness function: `fitness2` \
    Terminated after 5 iterations. \
    Terminated after 4 changes. \
    Number of evaluations: 505. \
    Goal reached? Yes \
    State cost: 4

- **Combination: NUM_POINTS=5000, NUM_SETS=5000, DENSITY=0.3**

    Algorithm: `tabu_search` \
    Fitness function: `fitness2` \
    Terminated after 16 iterations. \
    Terminated after 15 changes. \
    Number of evaluations: 1615. \
    Goal reached? Yes \
    State cost: 15

- **Combination: NUM_POINTS=5000, NUM_SETS=5000, DENSITY=0.7**

    Algorithm: `SAHCwReplacement` \
    Fitness function: `fitness2` \
    Terminated after 6 iterations. \
    Terminated after 5 changes. \
    Number of evaluations: 607. \
    Goal reached? Yes \
    State cost: 5

[^1]: The metric used is "best solution using the least number of fitness function calls (evaluations)".