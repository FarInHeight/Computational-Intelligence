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

## Results

**ALGORITHM**|**SIZE**|**DENSITY**|**#ITERATIONS**|**#CHANGES**|**#EVALUATIONS**|**STATE COST**
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
RMHC|100|0.3|2184|14|2185|8
SAHC|100|0.3|7|6|701|6
SAHC w/Replacement|100|0.3|7|6|701|6
Tabu Search|100|0.3|7|6|696|6
Simulated Annealing|100|0.3|5400|1726|5400|8
RMHC|100|0.7|2229|5|2230|3
SAHC|100|0.7|4|3|401|3
SAHC w/Replacement|100|0.7|4|3|401|3
Tabu Search|100|0.7|4|3|399|3
Simulated Annealing|100|0.7|5400|1470|5400|6
RMHC|1000|0.3|2823|23|2824|15 
SAHC|1000|0.3|11|10|11001|10
SAHC w/Replacement|1000|0.3|12|11|1211|11 
Tabu Search|1000|0.3|12|11|1210|11 
Simulated Annealing|1000|0.3|5400|1296|5400|20 
RMHC|1000|0.7|2006|6|2007|6
SAHC|1000|0.7|5|4|5001|4
SAHC w/Replacement|1000|0.7|6|5|607|5
Tabu Search|1000|0.7|5|4|505|4
Simulated Annealing|1000|0.7|5400|1364|5400|22
RMHC|5000|0.3|2024|22|2025|22 
SAHC|5000|0.3|14|13|70001|13
SAHC w/Replacement|5000|0.3|16|15|1617|15 
Tabu Search|5000|0.3|16|15|1615|15 
Simulated Annealing|5000|0.3|5400|1210|5400|322 
RMHC|5000|0.7|2093|9|2094|7
SAHC|5000|0.7|6|5|30001|5
SAHC w/Replacement|5000|0.7|6|5|607|5
Tabu Search|5000|0.7|7|6|707|6
Simulated Annealing|5000|0.7|5400|1183|5400|325

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