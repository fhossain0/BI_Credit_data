First Mesure if about BALANCE_FREQUENCY indicates how frequently the balance is updated or monitored. For this the calculated applied is 
''' 
Balance Frequency Segment = 
  SWITCH(
    TRUE(),
    'Table'[BALANCE_FREQUENCY] = 1, "High Frequency",
    'Table'[BALANCE_FREQUENCY] >= 0.5, "Medium Frequency",
    "Low Frequency"
  )
'''
