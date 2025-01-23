# knapsack-nl
A collection of $n$ objects is to be shipped, where each object has a weight $w_i$ and a value $v_i$. The goal is to pack a shipping container such that the total weight does not exceed the capacity $W$, and at most two items can be included in the container. Determine which items should be selected to maximize the total value of the container. Let $x_i$ represent whether object i is in included in the knapsack or not.

- **Objective:** Maximize the total value of the container

$$ \min - \sum_{i=0}^{n-1} v_i x_i $$

- **Constraint 1:** Total weight of the shipped container should not exceed the capacity weight

 $$  \sum_{i=0}^{n-1} w_i x_i  \leq W$$

- **Constraint 2:** At most two items can be included in the container

$$  \sum_{i=0}^{n-1} x_i  \leq 2$$


For this exercise, we will learn how to build the knapsack problem using the nonlinear model. Open up the code file `knapsack_nl.py`.  We created an array of binary variables symbol for five items. The value and weight of each item are defined in the values and weights constant symbols. The maximum capacity of the knapsack is set to 10. 

You will need to fill in the `set_sampler`and `build_nl` functions. Here are the instructions to follow:

   1. In the `set_sampler` function:

      - Define the sampler to be used. Remember to import any necessary packages.


   2. In the `build_nl` function:
   
      - Initialize the NL object called `model`, and import any necessary packages

      - Set the objective function in the NL model

      - Add the two constraints to the NL model


## License

Released under the Apache License 2.0. See [LICENSE](LICENSE) file.
