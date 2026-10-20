# DeFi & Blockchain — From Cryptography to Consensus

**Python · Cryptography · Probability · Blockchain simulations**

A growing collection of practical research assignments from a DeFi & Blockchain course. The goal is to connect blockchain mathematics with computational experiments — from Bitcoin key-space probabilities and Merkle proofs to Proof-of-Work mining.

> **Status:** HW1 and HW2 completed as student coursework; **instructor review pending**. HW3 is planned. This is an educational project, not a production blockchain or audited cryptographic library.

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?logo=jupyter&logoColor=white) ![Coursework](https://img.shields.io/badge/Coursework-Instructor_review_pending-orange)

## Research labs

| Lab | Research focus | Methods | Status |
|---|---|---|---|
| [HW1 · Cryptography](homeworks/hw01-cryptography/solution.ipynb) | Bitcoin key collisions, custom hashing, Merkle membership proofs | Monte Carlo, statistics, elliptic curves, SHA-256 comparison | Completed · Pending review |
| [HW2 · Proof of Work](homeworks/hw02-proof-of-work/solution.ipynb) | Nonce search, network mining, mining difficulty | Simulations, block hashes, hash-rate experiments | Completed · Pending review |
| [HW3 · Upcoming](homeworks/hw03-upcoming/) | To be announced | — | Planned |

## HW1 — Cryptography

**Question:** How small is the risk that a randomly generated Bitcoin private key duplicates an existing one?

For a key space of approximately `n−1` valid private keys and `N` existing keys, the first-order probability is approximately `P ≈ N / (n−1)`. The coursework investigates this estimate by experimenting with smaller elliptic-curve groups and comparing theory to observed collisions.

Other experiments: testing an original **educational** hash function for determinism, performance, avalanche effect, uniformity, chi-squared statistic, collisions and output-bit balance; implementing Merkle proof generation and membership verification.

**Important:** A home-built hash is not suitable for production cryptographic security. Statistical tests do not establish collision or preimage resistance.

**Explore:** [Open the HW1 notebook](homeworks/hw01-cryptography/solution.ipynb) · [Read the original assignment (transcribed)](homeworks/hw01-cryptography/assignment.md)

## HW2 — Proof of Work

**Question:** How do miner hash rates and difficulty influence block discovery?

Experiments include block construction, a Proof-of-Work nonce search, different peer hash rates and observed mining times across difficulty settings. For a simplified target requiring `d` leading hex zeroes in an ideal hash, a single independent attempt succeeds with probability `16^(−d)`, so the expected number of attempts is `16^d`.

**Attribution:** The exercise uses the third-party educational [BlockchainExample](https://github.com/0xBoringWozniak/BlockchainExample) library; the upstream blockchain implementation is not my original work.

**Methodology note:** Reported mining results are preliminary. Before drawing strong numerical conclusions, difficulty trials should use independent blocks / reset nonce and a consistent timing methodology.

**Explore:** [Open the HW2 notebook](homeworks/hw02-proof-of-work/solution.ipynb) · [Experiment notes](homeworks/hw02-proof-of-work/README.md)

## Skills

`Python` · `Jupyter` · `Monte Carlo` · `Probability & statistics` · `Hash functions` · `Merkle trees` · `Blockchain` · `Proof of Work` · `SageMath` · `Data visualization`

## Repository structure

```text
.
├── README.md
├── homeworks/
│   ├── hw01-cryptography/
│   │   ├── README.md
│   │   ├── solution.ipynb
│   │   └── assignment.md
│   ├── hw02-proof-of-work/
│   │   ├── README.md
│   │   └── solution.ipynb
│   └── hw03-upcoming/
│       └── README.md
└── .gitignore
```

## Reproducibility & limitations

Both original student notebooks are included with their saved outputs. The supplied HW1 assignment PDF is represented by a readable Markdown transcription. HW1 includes SageMath-specific computations, so some cells require a SageMath kernel rather than plain CPython. HW2 depends on the separately maintained BlockchainExample library. Python and package versions, seeds and CPU speed may change measured results; end-to-end reproducibility has not yet been established.

## Roadmap

- [x] HW1 — Cryptography and Merkle proofs
- [x] HW2 — Proof-of-Work experiments
- [x] Upload original notebooks and HW1 assignment transcription
- [ ] Export validated figures to README
- [ ] Validate experiments and provide a reproducible environment
- [ ] HW3 — Add the next completed assignment
- [ ] Add automated checks for mathematical invariants

## Academic integrity

This repository documents student coursework awaiting instructor review. Educational source code reused in HW2 is credited above. Experiments, claims and figures should not be interpreted as instructor-validated findings.
