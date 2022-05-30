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
* $(2 \cdot one) - 1$ one's
* $(2 \cdot two) - 1$ two's
* $(2 \cdot three) - 1$ three's
* $(2 \cdot four) - 1$ four's


$$((1+0) \cdot 1 + (2+1) \cdot 2 + (3+2) \cdot 3 + (4+3) \cdot 4 = 50 $$

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
 (7 + 5 + 3 + 1)  &- (& &  &(2 \cdot one - 1)) &one's \\
 (7 + 5 + 3 + 1)  &- (& &(2 \cdot two - 1) + &(2 \cdot one - 1)) &two's \\
 (7 + 5 + 3 + 1)  &- (&(2 \cdot three - 1) + &(2 \cdot two - 1) + &(2 \cdot  \cdot one - 1)) &three's \\
 (7 + 5 + 3 + 1)  &- ((2 \cdot four - 1) + &(2 \cdot three - 1) + &(2 \cdot two - 1) + &(2 \cdot one - 1)) &four's \\
\end{align}
 $$

The $(7 + 5 + 3 + 1)$ sub part  is $\sum_{i=1}^{n}(2n+1-(2i))$ where $n=4$. It can be expressed as
$$\sum_{i=1}^{n}(2n+1-(2i))$$
$$\sum_{i=1}^{n}(2n+1)-\sum_{i=1}^{n}(2i)$$
$$n(2n+1)-2\sum_{i=1}^{n}(i)$$
$$n(2n+1)-2\frac{n(n+1)}{2}$$
$$n(2n+1)-n(n+1)$$
$$n(2n+1-n-1)$$
$$n^2$$

So $(7 + 5 + 3 + 1)$ is $n^2$.


The remaining part

$$
\begin{align}
 &(                   &  &                    &  &                  &  &(2 \cdot one - 1)) &one's \\
 &(                   &  &                    &  &(2 \cdot two - 1) &+ &(2 \cdot one - 1)) &two's \\
 &(                   &  &(2 \cdot three - 1) &+ &(2 \cdot two - 1) &+ &(2 \cdot one - 1)) &three's \\
 &((2 \cdot four - 1) &+ &(2 \cdot three - 1) &+ &(2 \cdot two - 1) &+ &(2 \cdot one - 1)) &four's \\
\end{align}
$$

rewrittend as

$$
\begin{align}
 &(            &  &            &  &            &  &(2 \cdot 1) - 1) \cdot 1 &+ \\
 &(            &  &            &  &(2 \cdot 2) &+ &(2 \cdot 1) - 2) \cdot 2 &+ \\
 &(            &  &(2 \cdot 3) &+ &(2 \cdot 2) &+ &(2 \cdot 1) - 3) \cdot 3 &+ \\
 &((2 \cdot 4) &+ &(2 \cdot 3) &+ &(2 \cdot 2) &+ &(2 \cdot 1) - 4) \cdot 4 &  \\
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

Using $count \cdot (high+low) / 2$ for a summation from $low$ to $high$, with $low$ being always 1 and $count$ and $high$ being the same, we get:

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
$$\sum_{i=1}^{n}(i^3) = \frac{n^2(n+1)^2}{4}$$

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


