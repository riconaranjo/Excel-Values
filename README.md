# How to check if excel value is present in a list

This is the best way to check for an exact match:

    =IF(ISNUMBER(MATCH(B2,A:A,0)),"found","not found")

- `B2` is the cell you want to compare to the list.
- `A:A` means all values in the `A` column
- `0` means the type of comparison
  - [string comparisons seem to default to exact match]