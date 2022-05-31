Finding general formulas for picking the biggest/smallest values when rolling multiple dice.

---

Sometime, roll multiple dice and only pick some. What are the results?

In the game of Dungeon and Dragons (DnD), can have advantage (or disadvantage) on a roll. Instead of rolling a single 20 sided dice (d20), 2 d20's are rolled. In the case of advantage, the best result is used. In the case of disadvantage, it is the worst result that is used.

During character creation, many methods are available to generate characters abilities. The old school method was to roll 3 6 sided dices (3d6).

What is to be expected from this? Lets dig in.

# Notation Used

To indicate that 3 6 sided dices are rolled, the notation 3d6 will be used where the first number is the number of dice rolled and the second is number of sides (values) of the dice. So 1d20 indicate rolling a single twenty sided dice.

When selecting some of the rolled values, the number of values to retain and whether the biggest or smallest values will affect the result. To indicate "the lowest 2 values when rolling 3d6" will be expressed with "2s3d6" and "the biggest single die out of 5d8" will be "1b5d20". The value expressed will be the sum of the retained dice.

Nota: Parts of this document use "b" for best and "w" for worst instead of "b" for biggest and "s" for smallest.


# 1 of 2 dices

Click [here](Pick1of2.md) to consult the method used.


## Pick smallest dice out of 2 (Disadvantage)
$$ \frac{n(n+1)(2n+1)}{6n^2} $$

## Pick biggest dice out of 2 (Advantage)
$$ \frac{n(n+1)(4n-1)}{6n^2} $$


# 2 of 3 dices

Click [here](PickSmallest2of3.md.md) [here](PickBiggest2of3.md.md) to consult the method used.

## Pick smallest 2 dices out of 3 
$$ \frac{19n^4+22n^3+5n^2+2n}{24n^3}  $$

## Pick biggest 2 dices out of 3 

 $$ \frac{15n^2 + 30n + 3}{12n}$$

# Result

## Averages

The averages for various dices are:

| Dice | Worst 1 of 2 | 1 dice | Best 1 of 2 | | Worst 2 of 3 | 2 dices | Best 2 of 3 |
|-----:|-------------:|-------:|------------:|-|-------------:|--------:|------------:|
| d4   | 1.8750       | 2.5    | 3.1250      | | 4.1406       | 5       |  7.5625     |
| d6   | 2.5280       | 3.5    | 4.4720      | | 5.7037       | 7       | 10.0417     |
| d8   | 3.1875       | 4.5    | 5.8125      | | 7.2773       | 9       | 12.5313     |
| d10  | 3.8500       | 5.5    | 7.1500      | | 8.8550       | 11      | 15.0250     |
| d12  | 4.5139       | 6.5    | 8.4861      | | 10.4346      | 13      | 17.5208     |
| d20  | 7.1750       | 10.5   | 13.825      | | 16.7606      | 21      | 27.5125     |

## Equivalent modifiers
The condensed equivalent modifier versus the NTV:

| NTV      | Best/Worst 1 of 2 |
|---------:|------------------:|
| 2 or 20  | 0.95              |
| 3 or 19  | 1.80              |
| 4 or 18  | 2.55              |
| 5 or 17  | 3.20              |
| 6 or 16  | 3.75              |
| 7 or 15  | 4.20              |
| 8 or 14  | 4.55              |
| 9 or 13  | 4.80              |
| 10 or 12 | 4.95              |
|       11 | 5.00              |













