# Pick best 2 dices out of 3

## Pick best dice out of 2 on 1d4 is
| 1b2d4  | 1  | 2  | 3  | 4  |
|   ---  |--- |--- |--- |--- |
| 1      | 1  | 2  | 3  | 4  |
| 2      | 2  | 2  | 3  | 4  |
| 3      | 3  | 3  | 3  | 4  |
| 4      | 4  | 4  | 4  | 4  |

sum of all values is 
- 1+0 of one's
- 2+1 of two's
- 3+2 of three's
- 4+3 of four's

or again
* $(2*one) - 1$ one's
* $(2*two) - 1$ two's
* $(2*three) - 1$ three's
* $(2*four) - 1$ four's


$$((1+0)*1 + (2+1)*2 + (3+2)*3 + (4+3)*4 = 50 $$

Which gives 50

Now checking for best 2 dices out of 3

|(1)2b3d4| 1  | 2  | 3  | 4  |
|   ---  |--- |--- |--- |--- |
| 1      | 2  | 3  | 4  | 5  |
| 2      | 3  | 4  | 5  | 6  |
| 3      | 4  | 5  | 6  | 7  |
| 4      | 5  | 6  | 7  | 8  |

If we substract the values of "1b2d4" from "(1)2b3d4", we get

|    | 1  | 2  | 3  | 4  |
|--- |--- |--- |--- |--- |
| 1  | 1  | 1  | 1  | 1  |
| 2  | 1  | 2  | 2  | 2  |
| 3  | 1  | 2  | 3  | 3  |
| 4  | 1  | 2  | 3  | 4  |

which is the same as "1w2d4"

---

|(2)2b3d4| 1  | 2  | 3  | 4  |
|   ---  |--- |--- |--- |--- |
| 1      | 3  | 4  | 5  | 6  |
| 2      | 4  | 4  | 5  | 6  |
| 3      | 5  | 5  | 6  | 7  |
| 4      | 6  | 6  | 7  | 8  |

If we substract the values of "1b2d4" from "(1)2b3d4", we get

|    | 1  | 2  | 3  | 4  |
|--- |--- |--- |--- |--- |
| 1  | 2  | 2  | 2  | 2  |
| 2  | 2  | 2  | 2  | 2  |
| 3  | 2  | 2  | 3  | 3  |
| 4  | 2  | 2  | 3  | 4  |

Which is the similar to "1w2d4", execept that the first row and column changed from 1 to 2. So it's "1w2d4" plus 7 one's.


---

|(3)2b3d4| 1  | 2  | 3  | 4  |
|   ---  |--- |--- |--- |--- |
| 1      | 4  | 5  | 6  | 7  |
| 2      | 5  | 5  | 6  | 7  |
| 3      | 6  | 6  | 6  | 7  |
| 4      | 7  | 7  | 7  | 8  |

If we substract the values of "1b2d4" from "(1)2b3d4", we get

|    | 1  | 2  | 3  | 4  |
|--- |--- |--- |--- |--- |
| 1  | 3  | 3  | 3  | 3  |
| 2  | 3  | 3  | 3  | 3  |
| 3  | 3  | 3  | 3  | 3  |
| 4  | 3  | 3  | 3  | 4  |

---

|(4)2b3d4| 1  | 2  | 3  | 4  |
|   ---  |--- |--- |--- |--- |
| 1      | 5  | 6  | 7  | 8  |
| 2      | 6  | 6  | 7  | 8  |
| 3      | 7  | 7  | 7  | 8  |
| 4      | 8  | 8  | 8  | 8  |


---

**Some steps computed in a notebook should go here**

what remains after removing "1b2d4" and "1w2d4" from each 4 by 4 is 

* 7 one's for the second 4 by 4,
* 7 two's and 5 one's for the third 4 by 4,
* 7 three's, 5 two's and 3 one's for the fourth 4 by 4,

regrouping by values:

* $(7 + 5 + 3)$ one's
* $(7 + 5 )$ two's
* $(7)$ three's
* $(0)$ four's

Which can be expressed as

* $(7 + 5 + 3 + 1) - (1)$ one's
* $(7 + 5 + 3 + 1) - (3 + 1)$ two's
* $(7 + 5 + 3 + 1) - (5 + 3 + 1)$ three's
* $(7 + 5 + 3 + 1) - (7 + 5 + 3 + 1)$ four's

or

 $$
\begin{align}
 (7 + 5 + 3 + 1)  &- (& &  &(2*one - 1)) &one's \\
 (7 + 5 + 3 + 1)  &- (& &(2*two - 1) + &(2*one - 1)) &two's \\
 (7 + 5 + 3 + 1)  &- (&(2*three - 1) + &(2*two - 1) + &(2*one - 1)) &three's \\
 (7 + 5 + 3 + 1)  &- ((2*four - 1) + &(2*three - 1) + &(2*two - 1) + &(2*one - 1)) &four's \\
\end{align}
 $$

The $(7 + 5 + 3 + 1)$ sub part  is $\sum_{i=1}^{n}(2n+1-(2*i))$ where $n=4$. It can be expressed as
$$\sum_{i=1}^{n}(2n+1-(2*i))$$
$$\sum_{i=1}^{n}(2n+1)-\sum_{i=1}^{n}(2*i)$$
$$n(2n+1)-2\sum_{i=1}^{n}(i)$$
$$n(2n+1)-2\frac{n(n+1)}{2}$$
$$n(2n+1)-n(n+1)$$
$$n(2n+1-n-1)$$
$$n^2$$

So $(7 + 5 + 3 + 1)$ is $n^2$.


The remaining part

$$
\begin{align}
 &(               &                &              &(2*one - 1)) &one's \\
 &(               &                &(2*two - 1) + &(2*one - 1)) &two's \\
 &(               &(2*three - 1) + &(2*two - 1) + &(2*one - 1)) &three's \\
 &((2*four - 1) + &(2*three - 1) + &(2*two - 1) + &(2*one - 1)) &four's \\
\end{align}
$$

rewrittend as

$$
\begin{align}
 &(              &              &              &(2 \cdot 1) - 1) & \cdot 1 + \\
 &(              &              &(2 \cdot 2) + &(2 \cdot 1) - 2) & \cdot 2 + \\
 &(              &(2 \cdot 3) + &(2 \cdot 2) + &(2 \cdot 1) - 3) & \cdot 3 + \\
 &((2 \cdot 4) + &(2 \cdot 3) + &(2 \cdot 2) + &(2 \cdot 1) - 4) & \cdot 4   \\
\end{align}
$$

then as

$$
\begin{align}
 &( &2 ( 1) - 1) & \cdot 1 + \\
 &( &2 ( 1 + 2 ) - 2) & \cdot 2 + \\
 &( &2 ( 1 + 2 + 3) - 3) & \cdot 3 + \\
 &( &2 ( 1 + 2 + 3 + 4) - 4) & \cdot 4   \\
\end{align}
$$

Using $count*(high+low) / 2$ for a summation from $low$ to $high$, with $low$ being always 1 and $count$ and $high$ being the same, we get:

$$
\begin{align}
 ( \frac{2 \cdot 1(1+1)}{2} - 1) & \cdot 1 + \\
 ( \frac{2 \cdot 2(2+1)}{2} - 2) & \cdot 2 + \\
 ( \frac{2 \cdot 3(3+1)}{2} - 3) & \cdot 3 + \\
 ( \frac{2 \cdot 4(4+1)}{2} - 4) & \cdot 4   \\
\end{align}
$$

simplifying

$$
\begin{align}
 ( 1(1+1) - 1) & \cdot 1 + \\
 ( 2(2+1) - 2) & \cdot 2 + \\
 ( 3(3+1) - 3) & \cdot 3 + \\
 ( 4(4+1) - 4) & \cdot 4   \\
\end{align}
$$

simplifying

$$
\begin{align}
 ( (1+1) - 1) & \cdot 1^2 + \\
 ( (2+1) - 1) & \cdot 2^2 + \\
 ( (3+1) - 1) & \cdot 3^2 + \\
 ( (4+1) - 1) & \cdot 4^2   \\
\end{align}
$$

simplifying

$$
\begin{align}
 ( 1 ) & \cdot 1^2 + \\
 ( 2 ) & \cdot 2^2 + \\
 ( 3 ) & \cdot 3^2 + \\
 ( 4 ) & \cdot 4^2   \\
\end{align}
$$

Ok! I didn't see that coming.

$$
\begin{align}
 1^3 &+ \\
 2^3 &+ \\
 3^3 &+ \\
 4^3 &  \\
\end{align}
$$

we are left with a summation of cubes, which is 
 $$\sum_{i=1}^{n}(i^3) = \frac{n^2(n+1)^2}{4}$$.

Regrouping all the parts.

The following where needed 4 times:

* "1b2d4": $ \frac{n(n+1)(4n-1)}{6} $
* "1w2d4": $ \frac{n(n+1)(2n+1)}{6} $
* $(7 + 5 + 3 + 1)$:  $n^2$ 

and  $ \frac{n^2(n+1)^2}{4}$ once.
where $n=4$

Together we get:

 $$ n \left(\frac{n(n+1)(4n-1)}{6} + \frac{n(n+1)(2n+1)}{6} + n^2\right) + \frac{n^2(n+1)^2}{4}$$
 $$ n^2 \left(\frac{(n+1)(4n-1) + (n+1)(2n+1) + 6n}{6} + \frac{(n+1)^2}{4}\right)$$
 $$ \frac{n^2}{12} \left(2(n+1)(4n-1) + 2(n+1)(2n+1) + 12n + 3(n+1)^2\right)$$
 $$ \frac{n^2}{12} \left((n+1)\left(2(4n-1) + 2(2n+1) + 3(n+1)\right) + 12n\right)$$
 $$ \frac{n^2}{12} \left((n+1)\left(8n-2 + 4n+2 + 3n+3\right) + 12n\right)$$
 $$ \frac{n^2}{12} \left((n+1)\left(8n + 4n + 3n-2+2+3\right) + 12n\right)$$
 $$ \frac{n^2}{12} \left((n+1)\left(15n+3\right) + 12n\right)$$
 $$ \frac{n^2}{12} \left(15n^2 + 18n + 3 + 12n\right)$$
 $$ \frac{n^2}{12} \left(15n^2 + 30n + 3\right)$$

Is the total, for the average, divide by $n^3$ to get
 $$ \frac{15n^2 + 30n + 3}{12n}$$


---
---
---






Grand total  of  $268 + 331 + 392 + 450 + 504 + 553 + 596 + 632 = 3726$

---
Regrouping by value (all the one's together, etc) and summing it all toghether gives us the following:


- 64 + 8*(8+7) - (1+2+3+4+5+6+7) of one's
- 64 + 8*(7+6) - (1+2+3+4+5+6) of two's
- 64 + 8*(6+5) - (1+2+3+4+5) of three's
- 64 + 8*(5+4) - (1+2+3+4) of four's
- 64 + 8*(4+3) - (1+2+3) of five's
- 64 + 8*(3+2) - (1+2) of six's
- 64 + 8*(2+1) - (1) of seven's
- 64 + 8*(1+0) - (0) of eight's

There seems to be a relation between the value of the result and its occurence


 $$
\begin{align}
(64 &+ 8*((2*8 + 1) &- (2 * one))   &- (1+2+3+4+5+6+7)) one's \\
(64 &+ 8*((2*8 + 1) &- (2 * two))   &- (1+2+3+4+5+6)) two's \\
(64 &+ 8*((2*8 + 1) &- (2 * three)) &- (1+2+3+4+5)) three's \\
(64 &+ 8*((2*8 + 1) &- (2 * four))  &- (1+2+3+4)) four's \\
(64 &+ 8*((2*8 + 1) &- (2 * five))  &- (1+2+3)) five's \\
(64 &+ 8*((2*8 + 1) &- (2 * six))   &- (1+2)) six's \\
(64 &+ 8*((2*8 + 1) &- (2 * seven)) &- (1)) seven's \\
(64 &+ 8*((2*8 + 1) &- (2 * eight)) &- (0)) eight's
\end{align}
 $$


Using $count*(high+low) / 2$ for a summation from low to high, with $low$ being always 1 and $count$ and $high$ being the same, we get:

 $$
\begin{align}
(64 &+ 8*((2*8 + 1) &- (2 * one))   &- ((8-one)*(8-one+1) / 2)) one's \\
(64 &+ 8*((2*8 + 1) &- (2 * two))   &- ((8-two)*(8-two+1) / 2)) two's \\
(64 &+ 8*((2*8 + 1) &- (2 * three)) &- ((8-three)*(8-three+1) / 2)) three's \\
(64 &+ 8*((2*8 + 1) &- (2 * four))  &- ((8-four)*(8-four+1) / 2)) four's \\
(64 &+ 8*((2*8 + 1) &- (2 * five))  &- ((8-five)*(8-five+1) / 2)) five's \\
(64 &+ 8*((2*8 + 1) &- (2 * six))   &- ((8-six)*(8-six+1) / 2)) six's \\
(64 &+ 8*((2*8 + 1) &- (2 * seven)) &- ((8-seven)*(8-seven+1) / 2)) seven's \\
(64 &+ 8*((2*8 + 1) &- (2 * eight)) &- ((8-eight)*(8-eight+1) / 2)) eight's
\end{align}
 $$

Using $n$ for the number of sides and $j$ for the current value, each line becomes:

 $$
(n^2 + n((2n + 1) - (2j)) - \frac{(n-j)(n-j+1)}{2})  j
 $$

regrouping the terms and simplifying:
 $$
(n^2 + n(2n + 1 - 2j) - \frac{(n-j)*(n-j+1)}{2})  j \\
(n^2 + 2n^2 + n - 2nj - \frac{(n-j)*(n-j+1)}{2})  j \\
(3n^2 + n - 2nj - \frac{n^2-2nj+n+j^2-j}{2})  j \\
\frac{6n^2 + 2n - 4nj -n^2+2nj-n-j^2+j}{2}  j \\
\frac{5n^2 + n + (1 - 2n)j -j^2 }{2}  j \\
\frac{5n^2 + n}{2}j + \frac{(1 - 2n)}{2}j^2 -\frac{1}{2}j^3 \\
$$


So, for all the values of $j$ we have:

$$
\sum_{j=1}^{n}(\frac{5n^2 + n}{2}j + \frac{(1 - 2n)}{2}j^2 -\frac{1}{2}j^3 ) \\
\frac{5n^2 +n}{2}\sum_{j=1}^{n}j + \frac{(1 - 2n)}{2}\sum_{j=1}^{n}j^2 - \frac{1}{2}\sum_{j=1}^{n}j^3 \\
\frac{5n^2 +n}{2}\frac{n(n+1)}{2} + \frac{(1 - 2n)}{2}\frac{n(n+1)(2n+1)}{6} - \frac{1}{2}\frac{n^2(n+1)^2}{4} \\
\frac{(5n^3 +n^2)(n+1)}{4} + \frac{(1 - 2n)n(n+1)(2n+1)}{12} - \frac{n^2(n+1)^2}{8} \\
\frac{19n^4+22n^3+5n^2+2n}{24}
$$



gives 3726

And the average value of the sum is:
$$
\frac{19n^4+22n^3+5n^2+2n}{24n^3}
$$

Average: $3726/8^3 = 7.27734375$


