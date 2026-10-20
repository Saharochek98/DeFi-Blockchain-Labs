# HW1 — Crypto: Assignment

This is a readable transcription of the instructor-provided one-page **HW 1. Crypto** assignment. It is included for educational context; the wording of the tasks is preserved.

## 1. Bitcoin wallet exploit (3 points)

- Calculate the probability of generating an already used private key in the Bitcoin network, given that a total of `10^8` keys are in use. Give the formula and numerical results.
- Verify the result experimentally on scaled-down versions of secp256k1. Here `b` denotes the bit length of the group order `n`, so `n ≈ 2^b`. The real secp256k1 has `b = 256`. For `b = 20, 24, …, 40`, find a prime `p` such that `y² = x³ + 7` over `F_p` has a prime number of points `n` with `b` bits. Choose a population size `N < n`, measure how often a newly generated key matches one of the `N` existing ones, and compare with your formula. Plot `log₂ P` against `b` and extrapolate to `b = 256`.

## 2. Implement your own hash function in Python (3 points)

Demonstrate the following properties on input data:

- Determinism
- Computation speed
- Avalanche effect
- Uniformity
- Chi-squared
- Collisions
- Bit balances

Describe advantages and disadvantages of the function based on benchmarks.

## 3. Merkle trees (4 points)

Based on the MerkleTree example from the seminar, implement:

- A method to generate a Merkle Proof.
- A method to verify whether a transaction is included in the tree.

For `tx2`, the full proof consists of:

- Sibling hash at the first level: `h(tx1)`
- Hash from the second level: `h(tx3, tx4)`

Source: instructor's **HW 1. Crypto** PDF provided with the submission.
