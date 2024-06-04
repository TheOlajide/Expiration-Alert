## Expiration alert for calibration of Oil and Gas metering system.



### Project Overview
---
In compliance with the Department of Petroleum Resources(DPR) regulation, it is compulsory to carry out routine calibration of oil and gas flow meters every six month.
This exercise checks the correctness of such meters using an international standard prover tank as gauge, after which adjustments can be made on metering system using a calculated mathematical value(K-factor).

This project aims to provide a solution that tracks and notifies oil and gas companies of the next due date for calibration. It was carried out using a simple excel spreadsheet, automated with formulas.

### Steps Taken;

1. Create a table or range with all necessary headings and values.

2. To get the next calibration date:

Previous calibration date
```
EDATE(previous calibration date, 6) = Next calibration date
```
Number of Monthly interval = 6

3. To format ‘Next Calibration Date’ column;
 - Conditional formatting
 - New formatting rule
 - Format only cells that contains…
```
Cell value >= EDATE(previous calibration date, 6)
```
 - Choose formatting color

4. To create a status column that tells wether calibration is 'DUE' or 'NOT DUE'.
```
If (Today() >= Next calibration date, “DUE”,”NOT DUE”)
```

5.To set ‘Days Remaining’ column

```
Next calibration date – Today()
````
