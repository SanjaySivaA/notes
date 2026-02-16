---
title: "DSA"
---

## Dynamic Programming

Dynamic programming can
be applied if the problem can be divided into overlapping subproblems that can
be solved independently.

Two uses:
    * Finding optimal solution
    * Counting number of solutions

### Types

1. Coin problem
2. Longest Increasing Subsequence
3. Paths in a grid
4. Knapsack
5. Edit distance
6. Counting tilings


## Greedy algorithms

Constructs a solution by making the 'best' choice at the moment.  The locally optimal choices
in a greedy algorithm should also be globally optimal. It is often difficult to argue
that a greedy algorithm works.

### 1. Coin problem

```md
    In case of euro coins {1, 2, 5, 10, 20, 50, 100, 200}

    We can show for each coin x that it is not possible  
    to optimally construct a sum x or any larger sum by only using coins that are  
    smaller than x. For example, if x = 100, the largest optimal sum using the smaller  
    coins is 50+20+20+5+2+2 = 99. Thus, the greedy algorithm that always selects  
    the largest coin produces the optimal solution.  
        
    **NOTE** - Greedy algorithm would **not** work in general case.  
            eg: 6 using {1, 3, 4}

    It is not known if the general coin problem can be solved using any greedy
    algorithm. However, it is possible to *check* in polynomial time if the greedy approach
    works for a given set of coins.
```

### 2.  Scheduling

Given n events with their starting and ending times, find a schedule that includes as many events as possible.

```md
    Appraoch: Select the next possible event that ends as soon as possible.

    Correctness argument: consider what happens if we
    first select an event that ends later than the event that ends as early as possible.
    Now, we will have at most an equal number of choices how we can select the next
    event.
```

### Tasks and Deadlines

Given n tasks with durations and deadlines. For each task, we earn d − x points where d is the task’s deadline and x is the moment when we
finish the task. Choose an order to perform the tasks. Find largest possible score.

```
    Surprisingly, the optimal solution to the problem does not depend on the
    deadlines at all, but a correct greedy strategy is to simply perform the tasks
    sorted by their durations in increasing order.

    
```