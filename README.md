[![Open in GitHub Codespaces](
  https://img.shields.io/badge/Open%20in%20GitHub%20Codespaces-333?logo=github)](
  https://codespaces.new/dwave-training/knapsack-nl?quickstart=1)

# NL Knapsack Exercise
A collection of $n$ objects is to be shipped, where each object has a weight $w_i$ and a value $v_i$. The goal is to pack a shipping container such that the total weight does not exceed the capacity $W$, and at most two items can be included in the container. Determine which items should be selected to maximize the total value of the container. Let $x_i$ represent whether object i is in included in the container or not.

- **Objective:** Maximize the total value of the container

$$ \min - \sum_{i=0}^{n-1} v_i x_i $$

- **Constraint 1:** Total weight of the shipped container should not exceed the capacity weight

 $$  \sum_{i=0}^{n-1} w_i x_i  \leq W$$

- **Constraint 2:** At most two items can be included in the container

$$  \sum_{i=0}^{n-1} x_i  \leq 2$$


This is an example of the knapsack problem. In this exercise, we will learn how to build this problem using the nonlinear-program solver. Open the `knapsack_nl.py` code file.  We have created an array of binary variable symbols for five items. The value and weight of each item is defined in the values and weights constant symbols. The maximum capacity of the container is set to 10. 

You will need to fill in the `set_sampler`and `build_nl` functions. Here are the instructions to follow:

   1. In the `set_sampler` function:

      - Define the sampler to be used. Remember to import any necessary packages.


   2. In the `build_nl` function:
   
      - Initialize the NL object called `model`, and import any necessary packages

      - Set the objective function in the NL model

      - Add the two constraints to the NL model
