# Nim Game (misère game)

To make it simple, Nim is a game in which two players compete on a field with a certain number of rows and matchsticks. \
Given that a row has index $i$, it will contain $2^i + 1$ matchsticks.

For example, `Nim(5)` (5 rows), we will have the following starting configutation:
```
1.                    |                     (1)
2.                |   |   |                 (3)
3.            |   |   |   |   |             (5)
4.        |   |   |   |   |   |   |         (7)
5.    |   |   |   |   |   |   |   |   |     (9)  
```

In each turn, each player must take at least one matchstick and from just one row. So a player can take 5 matchsticks from the 4th row but not 3 from the 4th and 2 from the 5th.

In our type of Nim, the player who wins is the one that has to take a matchstick but no one is left. In this way, a player needs to play in order to force the opponent to take the last matchstick.

### Optional modification (The subtraction game)

It is possible to add a constrain to the game defined above, i.e. we can limit each player to take at most $k$ matchsticks from each row. \
This additional constrain will cause the game to be slower and it will be more difficult to create a safe winning strategy.

## References

* [Nim](https://en.wikipedia.org/wiki/Nim)
* [How to win at Nim](https://en.wikipedia.org/wiki/Nim#Proof_of_the_winning_formula)
* [Additional reading about Nim](https://brilliant.org/wiki/nim/)

## Collaborations

To implement the Rule-based agent, I collaborated with [Davide Vitabile s330509](https://github.com/Vitabile/Computational-Intelligence/tree/main). \
After some time, [Alexandro Buffa s316999](https://github.com/ExalFabu/Computational-Intelligence/tree/main) joined us. He mainly collaborated with us to implement the Evolved agent using an _ES_ strategy.