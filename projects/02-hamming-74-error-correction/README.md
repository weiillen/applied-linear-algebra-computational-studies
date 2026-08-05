# Hamming (7,4) Error Correction

This study uses binary linear algebra to encode four data bits into seven-bit Hamming codewords, detect a single-bit error, identify its position from the syndrome, and recover the original data.

## What the notebook implements

- Hamming (7,4) encoding over arithmetic modulo 2;
- parity-check evaluation;
- syndrome-to-bit-position mapping;
- single-bit correction;
- bit-level reading and writing of binary files;
- reconstruction of an intentionally corrupted PDF.

## Linear-algebra connection

The code treats messages and codewords as vectors over GF(2). Valid codewords satisfy a parity-check relation of the form:

```text
H y = 0
```

When a single bit is corrupted, the nonzero syndrome corresponds to a column of `H`, identifying the error location.

## Preserved files

- `HW2_112006265.ipynb` - implementation notebook.
- `report/HW2_112006265.pdf` - handwritten derivation and answers.
- `data/corrupt_question_4b.pdf` - intentionally corrupted binary input.
- `output/fixed_question_4b_112006265.pdf` - recovered one-page PDF.

The corrupted input is expected not to open as a normal PDF before decoding.

## Recorded recovery result

The recovered document reveals a question asking for conditions under which all columns of the parity-check matrix are different. The handwritten report discusses unique nonzero binary columns and sufficient row count.

## Limitations

- The implementation is designed for single-bit correction.
- The preserved notebook assumes the input files are available under the filenames used in its cells.
- The report retains its original handwritten format and academic identifiers.
