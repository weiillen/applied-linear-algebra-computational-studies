# Verification Notes

Verification was limited to non-destructive inspection of the uploaded artifacts.

## Checks performed

- All four preserved notebooks parse successfully as Jupyter notebook format.
- None of the preserved notebooks contains a stored Python exception output.
- The Hamming-code input named `corrupt_question_4b.pdf` is intentionally not recognized as a valid PDF before recovery.
- The preserved recovered output is a readable one-page PDF.
- The icosahedron OBJ contains 12 vertices, 12 vertex normals, and 20 triangular faces.
- Both notebook preview images were extracted from already stored notebook outputs.
- Every preserved portfolio copy matches its uploaded source by SHA-256 hash.

## Re-execution status

The notebooks were not re-executed and overwritten.

A complete fresh rerun was not claimed because:

- the Markov-chain notebook requires NLTK data download;
- the flat-shading notebook depends on an animation writer;
- the SVD notebook references an image not included in the archive; and
- rerunning would create new outputs that could be confused with the historical submission.

The displayed numerical values and figures are therefore identified as recorded notebook or report outputs, not independently reproduced benchmarks.
