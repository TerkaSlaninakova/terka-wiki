## Optimization problems
Are problems dedicated to finding the best solution among many possible solutions. In practice this often means minimizing/minimizing some **objective function `f(x)`** and considering some **constraints** when working in a **search space**. Mathematically speaking, the goal is to `find s* in S, such that f(s*) <= f(s) for all s in S`
We often find solution to these kinds of prolbems using [Metaheuristics](https://en.wikipedia.org/wiki/Metaheuristic) - heuristics that help us find sutiable heuristics that we can directly apply to the problem. They are welll suited, because they make few assumptions are are more generically applicable to a larger array of problems. On the other hand there are [optimization algorithms an iterative methods](https://en.wikipedia.org/wiki/Optimization_algorithm), that follow a more specific definition of a problem.

## Metaheuristics
* Inspired by nature (evolution, bees, ant colonies, hives, annealing)
* Using memory
* Deterministic/stochastic
* Population-based/individualistic
* Iterative

### Concepts:
1. Representation (coding) - e.g. binary coding where with every decision variable 1 binary value is associated
2. **Objective function** (účelová funkcia) - coming straight from the problem formulation / modified
3. Working with **constraints**
4. Parameter initialization and experimental analysis of algorithms


### Metaheristics working with 1 solution

```
In: initial solution s_0
t = 0;
repeat
    generate set of candidate solutions (C(s))
    choose one to be the current one (s_t)
    t += 1
until ending_condition
Out: The best found solution
```
The choice of initial solution is important, but better ones don't always lead to better **[local optimum](https://en.wikipedia.org/wiki/Local_optimum)** - solution that is optimal within a neighboring set of candidate solutions. neighborhood is a mapping of solutions `S -> 2^S` that assigns `N(s)` to every solution (e.g. k-distance in Travelling salesman problem).

