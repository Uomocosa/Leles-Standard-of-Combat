Go to a online python IDE.
Past the following code.
Run the program.

```python
# Online Python - IDE, Editor, Compiler, Interpreter
import random

def d20(): # roll a d20
    return random.randint(1, 20)
    
def advantage():  # roll 2d20 and take the highest
    return max(d20(), d20())
    
def disadvantage():  # roll 2d20 and take the lowest
    return min(d20(), d20())

def double_advantage():
    return max(d20(), d20(), d20())

def triple_advantage():
    return max(d20(), d20(), d20(), d20())
    
roll = advantage; 
# Change the previous line to 'roll = d20' to see the average value of a d20.
# Do the same with 'roll = double_advantage', ... to see their averages.

# Calculate the average
average = 0;
N = 100000;
for _ in range(0, N):
    average += roll()/N

print(f'average: {average}')
```