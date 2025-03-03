This Python program implements a Genetic Algorithm (GA) to find the maximum value of the Peak Function, which is a mathematical function with multiple local maxima and minima. The goal is to optimize 
𝑥
x and 
𝑦
y within a given range to achieve the highest function value.

Understanding the Code
1. Peak Function Definition
The function being optimized is:

𝑓
(
𝑥
,
𝑦
)
=
(
(
1
−
𝑥
)
2
𝑒
−
(
𝑥
2
)
−
(
𝑦
+
1
)
2
)
−
(
(
𝑥
−
𝑥
3
−
𝑦
3
)
𝑒
−
(
𝑥
2
)
−
(
𝑦
2
)
)
f(x,y)=((1−x) 
2
 e 
−(x 
2
 )−(y+1) 
2
 
 )−((x−x 
3
 −y 
3
 )e 
−(x**2)−(y**2))

This function has multiple peaks and valleys, making it a good test case for optimization algorithms.

2. Genetic Algorithm Parameters
Population Size (N = 60): The number of candidate solutions (individuals) in each generation.
Crossover Probability (Pc = 0.7): Determines how often crossover (genetic recombination) occurs.
Mutation Probability (Pm = 0.1): Probability of applying mutation to an individual.
Number of Generations (num_generations = 20): The number of iterations before the algorithm stops.
3. Initialization
The population is initialized randomly within the given range:
𝑥
,
𝑦
∈
[
−
3
,
3
]
x,y∈[−3,3]
Each individual in the population is a tuple 
(
𝑥
,
𝑦
)
(x,y).
4. Evolution Process (Main Loop)
For each generation, the following steps occur:

Fitness Evaluation
Each individual's fitness is calculated using the peak function.

Selection (Elitism Approach)

The individuals are sorted based on their fitness.
The top half of the population is selected as parents.
Crossover (Recombination)

Two random parents are chosen.
A one-point crossover is performed (swapping either the x-coordinate or y-coordinate).MutationWith probability 
𝑃
𝑚
P 
m
​
 , an individual undergoes mutation by assigning new random values for x and y.
Population Update

The next generation consists of mutated offspring and selected parents.
Progress Reporting

The best fitness value in each generation is printed.
5. Finding the Optimal Solution
At the end of the evolution process, the best individual in the final population is selected.
The corresponding x,y values and function output are displayed.
Possible Improvements
Tournament Selection or Roulette Wheel Selection: More sophisticated selection methods could be used.
Adaptive Mutation Rate: Adjusting 
𝑃
𝑚
P 
m
​
  dynamically based on progress.
Increasing Generations: Running for more generations may improve results.
