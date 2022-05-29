
Sometime, roll multiple dice and only pick some. What are the results?
In DnD, can have advantage (or disadvantage) on a roll. Instead of rolling a single 20 sided dice (d20), 2 d20's are rolled. In the case of advantage, the best result is used. In the case of disadvantage, it is the worst result that is used.

During character creation, many methods are available to generate characters abilities. The old school method was to roll 3 6 sided dices (3d6)

What is to be expected from this? Lets dig in.

# 1 of 2 dices


## Pick worst dice out of 2 (Disadvantage)
$$ \frac{n(n+1)(2n+1)}{6n^2} $$

## Pick best dice out of 2 (Advantage)
$$ \frac{n(n+1)(4n-1)}{6n^2} $$


# 2 of 3 dices

## Pick worst 2 dices out of 3 
$$ \frac{19n^4+22n^3+5n^2+2n}{24n^3}  $$

## Pick best 2 dices out of 3 

 $$ \frac{15n^2 + 30n + 3}{12n}$$

# Result

## Averages

The averages for various dices are:

| Dice | Worst 1 of 2 | 1 dice | Best 1 of 2 | | Worst 2 of 3 | 2 dices | Best 2 of 3 |
|-----:|-------------:|-------:|------------:|-|-------------:|--------:|------------:|
| d4   | 1.8750       | 2.5    | 3.1250      | | 4.1406       | 5       | x           |
| d6   | 2.5280       | 3.5    | 4.4720      | | 5.7037       | 7       | x           |
| d8   | 3.1875       | 4.5    | 5.8125      | | 7.2773       | 9       | x           |
| d10  | 3.8500       | 5.5    | 7.1500      | | 8.8550       | 11      | x           |
| d12  | 4.5139       | 6.5    | 8.4861      | | 10.4346      | 13      | x           |
| d20  | 7.1750       | 10.5   | 13.825      | | 16.7606      | 21      | x           |

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












