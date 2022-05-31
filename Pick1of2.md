
# Smallest 1 of 2 (Disadvantage)

What is the result of rolling 2 dice and selecting the worst value?



Rolling 2d4, selecting the lowest value give:

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | 1 | 1 | 1 | 1 |
| 2 | 1 | 2 | 2 | 2 |
| 3 | 1 | 2 | 3 | 3 |
| 4 | 1 | 2 | 3 | 4 |

Talling the occurence of each values:

* $7$ one's
* $5$ two's
* $3$ three's
* $1$ four's

To get the average of 1d4 with disadvantage, get the total for all the cases, 30 ($ 7 \cdot 1 + 5 \cdot 2 + 3 \cdot 3 + 1 \cdot 4$) and divide it by the number of cases, 16, so $\frac{30}{16}$ to get $1,875$.

Expressing the frequency (number of occurence) of a result (ex: 5) with the size of the dice, here 4, and the value of the result (ex: two) [(steps)](Pick1of2_Steps#Smallest_Relation).

* $(2 \cdot 4 + 1) - (2 \cdot one)$ one's
* $(2 \cdot 4 + 1) - (2 \cdot two)$ two's
* $(2 \cdot 4 + 1) - (2 \cdot three)$ three's
* $(2 \cdot 4 + 1) - (2 \cdot four)$ four's

The relation between the frequency and the value becomes appareant and can be expressed as $((2n+1) - (2i)) i$, where $i$ is the value of the result and $n$ the size of the dice. The sum of all the results is $\sum_{i=1}^{n}(((2n+1) - (2i)) i)$. Dividing it by the number of results, $n^2$, produce the average $\frac{1}{n^2}\sum_{i=1}^{n}(((2n+1) - (2i)) i)$, which can be [simplified](Pick1of2_Steps#Smallest_Simplification) to




$$ \frac{n(n+1)(2n+1)}{6n^2} $$

For our initial situation of rolling 1d4 with disadvantage, using the previous equation  with $n=4$ gives $1.875$

# Biggest 1 of 2 (Advantage)

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | 1 | 2 | 3 | 4 |
| 2 | 2 | 2 | 3 | 4 |
| 3 | 3 | 3 | 3 | 4 |
| 4 | 4 | 4 | 4 | 4 |

Rolling 2d4 with sadvantage give:

* $1$ one's
* $3$ two's
* $5$ three's
* $7$ four's

Expressing the frequency of a result (ex: 3) with the value of that result (ex: two)

* $(2 \cdot one) - 1$ one's
* $(2 \cdot two) - 1$ two's
* $(2 \cdot three) - 1$ three's
* $(2 \cdot four) - 1$ four's

The relation between the frequency and the value becomes appareant and can be expressed as $(2i-1)i$. The sum of all the results is $\sum_{i=1}^{n}(2i-1)i$. Dividing it by the number of results, $n^2$, produce the average $\frac{1}{n^2}\sum_{i=1}^{n}(2i-1)i$, which can be [simplified](PickBiggest1of2Steps) to

$$ \frac{n(n+1)(4n-1)}{6n^2} $$

For our initial situation of rolling 1d4 with disadvantage, using the previous equation  with $n=4$ gives $3.125$


# Change Title

Usually, player will roll a dice, add some modifier and compare it to a target value. For example, a player doing an attack roll will roll a d20, add his proficiency bonus, add any other bonuses, and compare it to the target value. Instead of adding any modifier to the dice roll, we can substract them from the target valuer. We will designate that as the Net Target Value (NTV).

## Odds agains a Net Target Value
We will investigate the odds against a NTV when rolling d20.

Using a single d20, the odds of getting a NTG or greater are:

|NTG|Odds (/20)|Odds (%)|
|---|----|----|
| 20 | 1/20 | 5% |
| 19 | 2/20 | 10% |
| 18 | 3/20 | 15% |
| 17 | 4/20 | 20% |
| 16 | 5/20 | 25% |
| 15 | 6/20 | 30% |
| 14 | 7/20 | 35% |
| 13 | 8/20 | 40% |
| 12 | 9/20 | 45% |
| 11 | 10/20 | 50% |
| 10 | 11/20 | 55% |
| 9 | 12/20 | 60% |
| 8 | 13/20 | 65% |
| 7 | 14/20 | 70% |
| 6 | 15/20 | 75% |
| 5 | 16/20 | 80% |
| 4 | 17/20 | 85% |
| 3 | 18/20 | 90% |
| 2 | 19/20 | 95% |
| 1 | 20/20 | 100% |

What do those odds become when in an advantage or disadvantage situation?

## Advantage vs NTV

In an advantage situation, to beat a NTG of 20 can be done either by rolling a 20 on the first dice (1 out of 20 possible outcomes) and any value other value than a 20 on the second dice (19 out of 20 possible outcomes), or by rolling any value other value than a 20 on the first dice (19 out of 20 possible outcomes) and a 20 on the second dice (1 out of 20 possible outcomes) or by rolling a 20 on the first dice (1 out of 20 possible outcomes) and a 20 on the second dice (1 out of 20 possible outcomes). Toghether, the odds of beating a NTG of 20 are:

$$
\begin{align}
 x &= (1/20)(19/20) + (19/20)(1/20) + (1/20)(1/20) \\
 x &= (19/400) + (19/400) + (1/400) \\
 x &= (19+19+1)/400 \\
 x &= 39/400 \\
 x &= 9.75\%
\end{align} 
 $$

Using this method, we have to find all the possible ways to beat the NTV with one dice and not the other, do this for the reverse situation and then list all the way that both dice would beat the NTV. For a NTV of 19, that is 20 on the first and 20 on the second dice, 20 on the first and 19 on the second dice, 19 on the first and 20 on the second dice, and 19 on the first and 19 on the second dice. This will only be more and more combinaisons to consider as we lower the NTV.

Instead, lets determine the odds of failing agains a NTV, and substract this from 100%.

For a For a NTV  of 20, the odds of failing are: rolling 19 or lower on the first dice (19 out of 20 possible outcomes) and rolling 19 or lower on the second dice (19 out of 20 possible outcomes). This gives:

$$
\begin{align}
 x &= 100\% - (19/20)(19/20) \\
 x &= 100\% - 90.25\% \\
 x &= 9.75\%
\end{align} 
$$

For a NTV of 19, it just a matter of rolling a 18 or less on both dice, and substract this from 100%. And so on for lower NTVs.

|NTV|Odds (%)|
|---|----|
| 20 | 9.75 |
| 19 | 19 |
| 18 | 27.75 |
| 17 | 36 |
| 16 | 43.75 |
| 15 | 51 |
| 14 | 57.75 |
| 13 | 64 |
| 12 | 69.75 |
| 11 | 75 |
| 10 | 79.75 |
| 9 | 84 |
| 8 | 87.75 |
| 7 | 91 |
| 6 | 93.75 |
| 5 | 96 |
| 4 | 97.75 |
| 3 | 99 |
| 2 | 99.75 |
| 1 | 100 |


## Disadvantage vs NTV

In this situation, as we use the lowest dice, both rolled dices must be above the NTV to beat it.

To beat a NTV of 20, a 20 must be rolled on the first dice (1 out of 20 possible outcomes) and a 20 on the second dice (1 out of 20 possible outcomes). This gives:
$$
\begin{align}
 x &= (1/20)(1/20) \\
 x &= 1/400 \\
 x &= 0.75\%
\end{align} 
$$

To beat a NTV of 19, a 19 or better must be rolled on the first dice (2 out of 20 possible outcomes) and a 19 or better on the second dice (2 out of 20 possible outcomes). This gives:

$$
\begin{align}
 x &= (2/20)(2/20) \\
 x &= 4/400 \\
 x &= 1\%
\end{align} 
$$

## Analyzing the results

Lets bring back the odds as modifier on the dice roll versus the regular 1d20 roll for each NTV.

| NTV | Single d20 Odds (%) | Advantage Odds (%) | Advantage as modifier | Disadvantage Odds (%) | Disadvantage as modifier |
|----:|--------------------:|-------------------:|----------------------:|----------------------:|-------------------------:|
| 20  | 5.00                | 9.75               | 0.95                  | 0.25                  | -0.95                    |
| 19  | 10.00               | 19.00              | 1.80                  | 1.00                  | -1.80                    |
| 18  | 15.00               | 27.75              | 2.55                  | 2.25                  | -2.55                    |
| 17  | 20.00               | 36.00              | 3.20                  | 4.00                  | -3.20                    |
| 16  | 25.00               | 43.75              | 3.75                  | 6.25                  | -3.75                    |
| 15  | 30.00               | 51.00              | 4.20                  | 9.00                  | -4.20                    |
| 14  | 35.00               | 57.75              | 4.55                  | 12.25                 | -4.55                    |
| 13  | 40.00               | 64.00              | 4.80                  | 16.00                 | -4.80                    |
| 12  | 45.00               | 69.75              | 4.95                  | 20.25                 | -4.95                    |
| 11  | 50.00               | 75.00              | 5.00                  | 25.00                 | -5.00                    |
| 10  | 55.00               | 79.75              | 4.95                  | 30.25                 | -4.95                    |
| 9   | 60.00               | 84.00              | 4.80                  | 36.00                 | -4.80                    |
| 8   | 65.00               | 87.75              | 4.55                  | 42.25                 | -4.55                    |
| 7   | 70.00               | 91.00              | 4.20                  | 49.00                 | -4.20                    |
| 6   | 75.00               | 93.75              | 3.75                  | 56.25                 | -3.75                    |
| 5   | 80.00               | 96.00              | 3.20                  | 64.00                 | -3.20                    |
| 4   | 85.00               | 97.75              | 2.55                  | 72.25                 | -2.55                    |
| 3   | 90.00               | 99.00              | 1.80                  | 81.00                 | -1.80                    |
| 2   | 95.00               | 99.75              | 0.95                  | 90.25                 | -0.95                    |
| 1   | 100.00              | 100.00             | 0.00                  | 100.00                | 0.00                     |

We see:
- The modifier for advantage and disadvantage is the same for each NTV, with the opposite sign,
- About half the modifiers (9 out of 20), have a value over 4 (in absolute value). These are centered around NTV 11, from NTV 15 to NTV 7,
- Starting at NTV 11, the modifier values are a mirror copy of the values before NTV 11.


## Cheat sheet

The equivalent modifier for NTV can be condensed to:

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
