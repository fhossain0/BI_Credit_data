# Balance Frequency Segment calculated column

This column categorizes the **BALANCE_FREQUENCY** column from the `Table` into different frequency segments.

```DAX
Balance Frequency Segment = 
SWITCH(
    TRUE(),
    'Table'[BALANCE_FREQUENCY] = 1, "High Frequency",
    'Table'[BALANCE_FREQUENCY] >= 0.5, "Medium Frequency",
    "Low Frequency"
)
