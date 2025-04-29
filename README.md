# ds5100_project
This a repo of the final project for Programming for Data Science 

This Python package models a customizable dice game simulation. It includes functionality to define weighted dice, simulate games with multiple dice, and analyze results for statistical patterns.

Metadata: 

- **Project Name**: Final Project 
- **Author**: Jasmine Waller
- **Language**: Python 
- **Dependencies**: 
  - numpy
  - pandas
  - collections
- **Structure**:
  - `Die` class for creating and rolling weighted dice
  - `Game` class for simulating rolls with multiple dice
  - `Analyzer` class for statistical analysis of game results

Synopsis:

1. Die Class

from Projectclasses import Die

faces = np.array(['A', 'B', 'C'])
my_die = Die(faces)
my_die.change_weight('B', 5.0)
rolls = my_die.roll_die(10)
print(rolls)

2. Game Class

from Projectclasses import Game

die1 = Die(np.array(['H', 'T']))
die2 = Die(np.array(['H', 'T']))
game = Game([die1, die2])
game.play(5)
print(game.game_results(form='wide'))

3. Analyzer Class 

from Projectclasses import Analyzer

analyzer = Analyzer(game)
print(analyzer.jackpot())
print(analyzer.permutation_count())
print(analyzer.combo_count())
print(analyzer.roll_count())

API: 

**Die Class**
- change_weight(face, new_weight): A method to change the weight of a single side
- roll_die(num_rolls=1): A method to roll the die one or more times
- show_die(): A method to show the die’s current state

**Game Class** 
- play(num_rolls): Play the game by rolling all dice a specified number of times.
- game_results(form='wide'): A method to show the user the results of the most recent play

**Analyze Class**
- jackpot():Checks to see how many times all the faces have the same value
- roll_count(): Counts how many times a given face is rolled in each event
- combo_count(): Counts the number of combinations 
- permutation_count(): Counts the number of permutations 
