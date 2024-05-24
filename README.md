# Empire State Building Bet

Imagine the following scenario: you're walking up the Empire State Building to DataCamp Headquarters and you're playing a game with a friend.

You throw a die one hundred times.

- If it's 1 or 2, you'll go one step down.
- If it's 3, 4, or 5, you'll go one step up.
- If you throw a 6, you'll throw the die again and will walk up the resulting number of steps.

Of course, you cannot go lower than step number 0. Also, you admit that you're a bit clumsy and have a chance of 0.1% of falling down the stairs when you make a move. Falling down means that you have to start again from step 0.

With all of this in mind, you bet with your friend that you'll reach 60 steps high.

## How to Solve?

What is the chance that you will win this bet? It's a complex assignment. One way to solve it would be to calculate the chance analytically using equations. Another possible approach is to simulate this process thousands of times and see in what fraction of the simulations you will reach 60 steps. This is a form of *hacker statistics*. As you can probably guess, we're going to opt for the second approach.

### Can you fill in the missing pieces to finish the script?

```python
# In the Empire State Building bet, your next move depends on the number you get after throwing the dice.
# We can perfectly code this with an if-elif-else construct!

# The sample code assumes that you're currently at step 50. 
# Can you fill in the missing pieces to finish the script? 
# numpy is already imported as np and the seed has been set to 123, so you don't have to worry about that anymore.

# NumPy is imported, seed is set
import numpy as np
# Starting step
step = 50

# Roll the dice
dice = np.random.randint(1, 7)

# Finish the control construct
if dice <= 2 :
    step = step - 1
elif dice <= 5 :
    step = step + 1
else :
    step = step + np.random.randint(1, 7)

# Print out dice and step
print(dice, step)
