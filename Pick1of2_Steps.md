# Smallest Relation

* $7$ one's
* $5$ two's
* $3$ three's
* $1$ four's


But, we notice that it relates with the max value of the dice, here 4, actually twice that, so 8.

* $((2 \cdot 4) - 1)$ one's
* $((2 \cdot 4) - 3)$ two's
* $((2 \cdot 4) - 5)$ three's
* $((2 \cdot 4) - 7)$ four's

There seems to be a relation between the value of the result and its occurence

* $(2 \cdot 4) - (2 \cdot one - 1)$ one's
* $(2 \cdot 4) - (2 \cdot two - 1)$ two's
* $(2 \cdot 4) - (2 \cdot three - 1)$ three's
* $(2 \cdot 4) - (2 \cdot four - 1)$ four's

or

* $(2 \cdot 4 + 1) - (2 \cdot one)$ one's
* $(2 \cdot 4 + 1) - (2 \cdot two)$ two's
* $(2 \cdot 4 + 1) - (2 \cdot three)$ three's
* $(2 \cdot 4 + 1) - (2 \cdot four)$ four's

Let use n for the max value of the dice, here 4, and move the +1 with it as it doesn't depend on the value of the result.

* $(2n + 1) - (2 \cdot one)$ one's
* $(2n + 1) - (2 \cdot two)$ two's
* $(2n + 1) - (2 \cdot three)$ three's
* $(2n + 1) - (2 \cdot four)$ four's


# Smallest Simplification

$$ \frac{1}{n^2}\sum_{i=1}^{n}(((2n+1) - (2i)) i) $$

Applying $i$ to each sub parts we get

$$ \frac{1}{n^2}\sum_{i=1}^{n}((2n+1)i - 2i^2) $$

Lets break apart the two parts, and move the constant part out of the summation.

$$ \frac{1}{n^2}\left((2n+1)\sum_{i=1}^{n}(i) - 2 \sum_{i=1}^{n}(i^2)\right) $$

## Solving

The summation of sequential numbers is $\frac{n(n+1)}{2}$. This will replace $\sum_{i=1}^{n}(i)$. The summation of squares is $\frac{n(n+1)(2n+1)}{6}$, which will replace $\sum_{i=1}^{n}(i^2)$. This leave us with:

$$ \frac{1}{n^2}\left((2n+1)\frac{n(n+1)}{2} - 2 \frac{n(n+1)(2n+1)}{6}\right) $$

Lets clean it up

$$ \frac{1}{n^2}\left(\frac{n(n+1)(2n+1)}{2} - \frac{2n(n+1)(2n+1)}{6}\right) $$

Isolating the common part $n(n+1)(2n+1)$, we get:

$$ \frac{n(n+1)(2n+1)}{n^2}  (\frac{1}{2} - \frac{2}{6}) $$

Changing $\frac{1}{2} - \frac{2}{6}$ to $\frac{1}{6}$:

$$ \frac{n(n+1)(2n+1)}{6n^2} $$