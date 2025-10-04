Implemented a calculated column in Power BI to categorize BALANCE_FREQUENCY using a conditional column   (SWITCH(TRUE(), …)):

High Frequency → BALANCE_FREQUENCY = 1

Medium Frequency → BALANCE_FREQUENCY >= 0.5

Low Frequency → BALANCE_FREQUENCY < 0.5

This helps in classifying customer balances for analysis and reporting purposes.

"The column was not created by a DAX measure, because a DAX measure does not create columns. Measures are used only for calculations and visualizations, not to store data in a table."
For better understanding here is the code 

```DAX
FrequencyCategory =
SWITCH(
    TRUE(),
    'Table'[BALANCE_FREQUENCY] = 1, "High Frequency",
    'Table'[BALANCE_FREQUENCY] >= 0.5, "Medium Frequency",
    'Table'[BALANCE_FREQUENCY] < 0.5, "Low Frequency"
)

Why True ?

Reason :
2. Using SWITCH(TRUE(), …)

TRUE() is a trick that lets you use logical conditions instead of exact matches.

Now each line can be a condition that evaluates to TRUE or FALSE.

```
