# Analysis boundary

Exploratory notebooks may be used to understand data, but the final analysis should be
implemented as parameterized scripts under `src/` with synthetic tests.

The canonical pipeline should:

1. validate the sample manifest;
2. perform segmentation or import registered measurements;
3. produce object-, image-, and device-level QC;
4. aggregate at the correct experimental unit;
5. fit the preregistered statistical model; and
6. export a machine-readable result table and a human-reviewable report.
