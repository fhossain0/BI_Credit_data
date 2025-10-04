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

Implemented a calculated column in Power BI to categorize BALANCE_FREQUENCY using a conditional column   (SWITCH(TRUE(), …)):

High Frequency → BALANCE_FREQUENCY = 1

Medium Frequency → BALANCE_FREQUENCY >= 0.5

Low Frequency → BALANCE_FREQUENCY < 0.5

This helps in classifying customer balances for analysis and reporting purposes.
