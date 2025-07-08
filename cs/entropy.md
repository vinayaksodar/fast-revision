# Information Theory

## Information

What exactly do we mean by *information*? Mathematically, the information content of an event with probability $p$ is defined as:

$$
\text{Information} = \log_2\left(\frac{1}{p}\right) = -\log_2(p)
$$

This tells us how *surprising* an event is: the less likely it is, the more information it carries when it occurs.
Note: Information as defined above is also called uncertainity sometimes

### Intuition with an Example

Suppose you're observing a group consisting of 4 men and 12 women (16 people in total). The probability of observing a man is:

$$
p(\text{man}) = \frac{4}{16} = \frac{1}{4}
$$

Then the information gained upon seeing a man is:

$$
\log_2\left(\frac{1}{1/4}\right) = \log_2(4) = 2 \text{ bits}
$$

This means observing a man reduces your uncertainty by 2 bits — you’ve narrowed your possible choices from 16 people to just the 4 men.

### Another Example: Rolling Two Dice

If you roll two standard 6-sided dice, there are 36 possible outcomes. Observing the exact outcome (e.g., a 3 and a 5) reduces the number of possibilities from 36 to 1.

$$
\log_2(36) \approx 5.17 \text{ bits}
$$

So, by seeing the outcome of the roll, you gain about 5.17 bits of information.

$\log_2(n)$ tells you how many binary yes/no questions you need to identify one of
n
n possibilities. So going from 36 to 1 means about 5.17 bits of information were gained — this is the maximum information for a uniform distribution of 36 outcomes.

$\log_2()$ is nothing special you can take any base binary plays well with base 2 but only the logarithm satisfies the required axioms:

- Continuity
- Additivity over independent events
- Maximality when probabilities are uniform

Note: the above intuition doesn't carry over well to a random variable there just think of it as the amount of surprise.

The term information or uncertainity can be slightly misleading here its just a random quantification of surprise not actual information of any sort. It doesn't refer to the semantic meaning or the practical knowledge you gain.

The term reduction in uncertainity is also misleading what was the uncertainity before??
Even if you think in terms of entropy it will be the average reduction in uncertainity not the uncertainity before.

## Entropy

In information theory, **entropy** $H(X)$ is the **average amount of information** contained in each piece of data received about a random variable $X$.

$$
H(X) = -\sum p(x) \log_2 p(x)
$$

## Encoding and Entropy

We have a random variable that takes values from the set {A, B, C, D}, with probabilities:

| Symbol | Probability | Ideal Code Length (-log₂(p)) |
| ------ | ----------- | ---------------------------- |
| A      | 1/3         | ≈ 1.585 bits                 |
| B      | 1/2         | 1.000 bits                   |
| C      | 1/12        | ≈ 3.585 bits                 |
| D      | 1/12        | ≈ 3.585 bits                 |

### Entropy

The entropy of the distribution is:

$$
H(X) = -\sum p(x) \log_2 p(x) \approx 1.792 \text{ bits per symbol}
$$

This is the theoretical lower bound on the **average** number of bits per symbol for any lossless encoding.

---

## Fixed-Length Encoding

Using 2 bits per symbol (since 4 symbols):

| Symbol | Code |
| ------ | ---- |
| A      | 00   |
| B      | 01   |
| C      | 10   |
| D      | 11   |

- Simple but **inefficient** — doesn’t reflect the symbol probabilities.
- Every symbol costs **2 bits**, even though B (with p = 1/2) only needs 1 bit ideally.

---

## Variable-Length Encoding (e.g. Huffman)

We can assign shorter codes to more frequent symbols:

| Symbol | Code | Length |
| ------ | ---- | ------ |
| B      | 0    | 1      |
| A      | 10   | 2      |
| C      | 110  | 3      |
| D      | 111  | 3      |

Expected bits per symbol:

$$
E[L] = \frac{1}{2}(1) + \frac{1}{3}(2) + \frac{1}{12}(3) + \frac{1}{12}(3) = 1.833 \text{ bits}
$$

Still above the entropy of 1.792 bits.

---

## Encoding Sequences

If we encode sequences like `AA`, `AB`, ..., `DD`, the combined probabilities better capture the structure, allowing more efficient Huffman coding.

- For long enough sequences, the **average bits per symbol** will converge to the entropy.
- But more importantly, the **number of bits used to represent each symbol** in a sequence will **converge to its ideal value**, `-log₂(p)`.

---

## Bit Cost Per Symbol Approaches Ideal

When encoding longer sequences (e.g. `AAABAC...`):

- Symbol `B`, which occurs 50% of the time, will take close to **1 bit** per occurrence.
- Symbol `A` (1/3) will take ≈ **1.585 bits** per occurrence.
- Symbols `C` and `D` (1/12 each) will take ≈ **3.585 bits** per occurrence.

In other words:

$$
\text{Bits used per occurrence of symbol } x \to -\log_2 p(x)
$$

as the sequence length increases and the encoder is optimized (e.g. via arithmetic coding or block Huffman coding).

---

## Summary

| Symbol | Probability | Ideal Bits (−log₂(p)) | Actual (Short Sequences) | Actual (Long Sequences) |
| ------ | ----------- | --------------------- | ------------------------ | ----------------------- |
| A      | 1/3         | ≈ 1.585               | \~2 bits                 | → 1.585 bits            |
| B      | 1/2         | 1.000                 | \~1 bit                  | → 1.000 bits            |
| C      | 1/12        | ≈ 3.585               | \~3 bits                 | → 3.585 bits            |
| D      | 1/12        | ≈ 3.585               | \~3 bits                 | → 3.585 bits            |

**Longer sequences + better encoding** →  
**Average bits per symbol → entropy**,  
**Per-symbol cost → ideal −log₂(p)**
