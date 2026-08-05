# Markov-Chain Text Generation

This notebook studies how an n-gram language model can be represented as a finite-state Markov chain.

## What the notebook implements

- text cleanup and lowercasing;
- word tokenization and n-gram generation;
- conversion between word-state tuples and matrix indices;
- construction and row normalization of a transition matrix;
- random text generation from an initial context;
- stationary-distribution estimation using power iteration.

The recorded experiment uses a short sentence about city performers, a 3-gram model, and three different generation lengths.

## Linear-algebra connection

For an n-gram model, each state consists of the previous `n - 1` words. Transition probabilities are stored in a row-stochastic matrix `P`. The notebook estimates a stationary distribution `pi` by repeatedly applying:

```text
pi_next = pi @ P
```

until the Euclidean change falls below a tolerance.

## Files

- `HW1_112006265.ipynb` - original notebook, unchanged.

## Limitations

- The example corpus is very small.
- The notebook constructs a dense state matrix whose size grows rapidly with vocabulary size and n-gram order.
- It downloads NLTK tokenizer data during execution.
- The recorded discussion and outputs are preserved as submitted and have not been silently corrected.
