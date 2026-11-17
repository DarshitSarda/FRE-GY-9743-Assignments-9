# FRE-GY-9743-Assignments-2026fall
Assignments for NYU, FRE-GY 9743, Fall 2026.

Assignment 9: open `Assignment9.ipynb`, the student notebook for PCA and swap hedging.

Use Python 3.11, install `requirements.txt`, and start Jupyter from the repository
root. Complete the 8 TODO blocks by replacing each `raise NotImplementedError(...)`
with your code, then restart the kernel and run all cells to generate your results.
Data loading, calibration, swap pricing, quote-risk calculations, and portfolio risk aggregation are provided; students assemble the hedge risk matrix.
Report formatting and plotting scaffolds are also provided.

Use all observations in `swap_data.xlsx`, through 2026-02-26. The workbook's
quotes are in percentage points; the provided code converts them to decimal rates.
For this assignment, all quotes and swaps follow the library's `USD-SOFR-OIS` convention.

The assignment has five parts:

1. Apply PCA with scikit-learn and select the smallest number of PCs explaining at least 99% of the variance.
2. Run the provided 2026-02-26 calibration, pricing, and quote-risk calculations, then assemble the hedge risk matrix.
3. Display PC loadings by original quote tenor, project portfolio and hedge risks into PC space, and reconstruct portfolio risk.
4. Calculate the PCA unweighted least-squares hedge and report instrument positions.
5. Calculate the PCA weighted least-squares hedge and report instrument positions.

Both hedges use 13 spot swaps: 1Y, 2Y, 3Y, 4Y, 5Y, 6Y, 7Y, 8Y, 9Y, 10Y, 12Y, 15Y, and 20Y.
PCA and quote-risk vectors retain all 15 quoted tenors, including 25Y and 30Y.
Quote DV01s come from the library's analytic state sensitivities and calibration
Jacobian.
