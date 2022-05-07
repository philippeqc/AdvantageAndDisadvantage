sdf
# Disadvantage

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | 1 | 1 | 1 | 1 |
| 2 | 1 | 2 | 2 | 2 |
| 3 | 1 | 2 | 3 | 3 |
| 4 | 1 | 2 | 3 | 4 |

Rolling 2d4 with disadvantage give:

* 7 ones
* 5 twos
* 3 threes
* 1 four

To get the average of 1d4 with disadvantage, get the total for all the cases, 30 ($ 7*1 + 5*2 + 3*3 + 1*4$) and divide it by the number of cases, 16, so $\frac{30}{16}$ to get $1,875$.



But, we notice that it relates with the max value of the dice, here 4, actually twice that, so 8.

* 8 - 1 ones
* 8 - 3 twos
* 8 - 5 threes
* 8 - 7 four

There seems to be a relation between the value of the result and its occurence

* 8 - (2*one - 1) ones
* 8 - (2*two - 1) twos
* 8 - (2*three - 1) threes
* 8 - (2*four - 1) four

or

* 8 + 1 - (2*one) ones
* 8 + 1 - (2*two) twos
* 8 + 1 - (2*three) threes
* 8 + 1 - (2*four) four

Let use n for the max value of the dice, here 4, and move the +1 with it as it doesn't depend on the value of the result.

* (2*n + 1) - (2 * one) ones
* (2*n + 1) - (2 * two) twos
* (2*n + 1) - (2 * three) threes
* (2*n + 1) - (2 * four) four

For each item, the frequency of a result is linked with the result. The number of ones found in the table is dependent on the value one. The number of twos depends on the value two, and so on. So with our 1d4, we have the values 1,2,3 and 4. We will identify this as `i`. And as we want to add it all together, we will use the summation symbolised by $\sum$.

$$ \sum_{i=1}^{n}(((2n+1) -(2*i))*i) $$

Applying $i$ to each sub parts
$$ \sum_{i=1}^{n}((2n+1)*i - 2*i^2) $$

Lets break apart the two parts, and move the constant part out of the summation.

$$ (2n+1)\sum_{i=1}^{n}(i) - 2 \sum_{i=1}^{n}(i^2) $$

## Solving

The summation of sequential numbers is $\frac{n(n+1)}{2}$. This will replace $\sum_{i=1}^{n}(i)$. The summation of squares is $\frac{n(n+1)(2n+1)}{6}$, which will replace $\sum_{i=1}^{n}(i^2)$. This leave us with:

$$ (2n+1)\frac{n(n+1)}{2} - 2 \frac{n(n+1)(2n+1)}{6} $$

Lets clean it up

$$ \frac{n(n+1)(2n+1)}{2} - \frac{2n(n+1)(2n+1)}{6} $$

Moving the common part $n(n+1)(2n+1)$, we get:

$$ n(n+1)(2n+1)  (\frac{1}{2} - \frac{2}{6}) $$

Changing $\frac{1}{2} - \frac{2}{6}$ to $\frac{1}{6}$:
$$ \frac{n(n+1)(2n+1)}{6} $$

is the total for all the cases. For the average, divide by the number of cases.

$$ \frac{n(n+1)(2n+1)}{6n^2} $$

## Result

$$ \frac{n(n+1)(2n+1)}{6n^2} $$

For our initial situation of rolling 1d4 with disadvantage, using the previous equation  with $n=4$ gives $1.875$

# Advantage

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | 1 | 2 | 3 | 4 |
| 2 | 2 | 2 | 3 | 4 |
| 3 | 3 | 3 | 3 | 4 |
| 4 | 4 | 4 | 4 | 4 |

Rolling 2d4 with sadvantage give:

* 1 ones
* 3 twos
* 5 threes
* 7 four

$1*1 + 3*2 + 5*3 + 7*4 = 50$

$$(2*one-1)*one + (2*two-1)*2 + (2*three-1)*three + (2*four-1)*four$$

$$\sum_{i=1}^{n}(2i-1)i$$
$$2\sum_{i=1}^{n}i^2 -\sum_{i=1}^{n}i$$

## Solving

$$2\sum_{i=1}^{n}i^2 -\sum_{i=1}^{n}i$$

becomes

$$ 2 \frac{n(n+1)(2n+1)}{6} - \frac{n(n+1)}{2} $$

Isolating $\frac{n(n+1)}{2}$

$$ \frac{n(n+1)}{2}( 2\frac{(2n+1)}{3} - 1) $$

$$ \frac{n(n+1)}{2}( \frac{4n+2}{3} - 1) $$
$$ \frac{n(n+1)}{2}( \frac{4n+2}{3} - \frac{3}{3}) $$
$$ \frac{n(n+1)(4n+2-3)}{6} $$
$$ \frac{n(n+1)(4n-1)}{6} $$

is the total for all the cases. For the average, divide by the number of cases.

$$ \frac{n(n+1)(4n-1)}{6n^2} $$



## Result

$$ \frac{n(n+1)(4n-1)}{6n^2} $$

For our initial situation of rolling 1d4 with disadvantage, using the previous equation  with $n=4$ gives $3.125$


---

  $$
  =  (2n-1)*1 + (2n-3)*2 + (2n-5)*3 + (2n-7)*4 \\
  =  (2n-(2i_1-1))*i_1 + (2n-(2i_2-1))*i_2 + (2n-(2i_3-1))*i_3 + (2n-(2i_4-1))*i_4 \\
 = (2n+1-2i_1)*i_1 + (2n+1-2i_2)*i_2 + (2n+1-2i_3)*i_3 + (2n+1-2i_4)*i_4 \\
 = (2n+1)(i_1 + i_2 + i_3 + i_4) - 2(i_1^2 + i_2^2 + i_3^2 + i_4^2) \\
 = (2n+1)\sum_{i=1}^{n=4}(i) - 2\sum_{i=1}^{n=4}(i^2) \\
 = (2n+1)\frac{n(n+1)}{2} - 2\frac{n(n+1)(2n+1)}{6} \\
 = \frac{n(n+1)(2n+1)}{2} - \frac{2n(n+1)(2n+1)}{6} \\
 = n(n+1)(2n+1)(\frac{1}{2} - \frac{2}{6}) \\
 = n(n+1)(2n+1)(\frac{3}{6} - \frac{2}{6}) \\
 = n(n+1)(2n+1)(\frac{3-2}{6}) \\
 = n(n+1)(2n+1)(\frac{1}{6}) \\
 $$

---

 $$
 = 7*1 + 5*2 + 3*3 + 1*4 \\
 = (2n-1)*1 + (2n-3)*2 + (2n-5)*3 + (2n-7)*4 \\
 = (2n-(2*1-1))*(n+1-1) + (2n-(2*2-1))*(n+1-2) + (2n-(2*3-1))*(n+1-3) + (2n-(2*4-1))*(n+1-4) \\
 = (2n-(2*i-1))*(n+1-i) + (2n-(2*i-1))*(n+1-i) + (2n-(2*i-1))*(n+1-i) + (2n-(2*i-1))*(n+1-i) \\
 = \sum_{i=1}^{n=4}(2n-(2*i-1))*(n+1-i) \\
  =  \sum_{i=1}^{n=4}(2n-(2*i-1))*(n+1-i) \\
  =  \sum_{i=1}^{n=4}(2n-2*i+1)*(n+1-i) \\
  $$
