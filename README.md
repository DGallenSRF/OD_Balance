# OD_Balance

Script requires three inputs:

* i x j matrix including the OD percentages from Streetlight.
* i x 1 matrix inlcuding the starting volumes.
* 1 x j matrix including the target volumes.

## Fix percentages

The script will first adjust each column of percentages incrementally by 1%. The goal is to ensure that the sum of each column subtracted from the target will result in less than 5 cars.

## Adjust to 100%

Each row must sum to 100%. We increment each row's lowest value to get the row's sum equal to 100%. 
This will affect our target differences, which are adjusted in the next step.

## Amend percentages

Adjust each percentages proportional to its total volume. Minimal error should remain. This final error from 100% (row sums) will be assigned to the final column of data.