
## File to refer: Employee Status.xlsb

Show the ‘Active/Inactive’ status of the employee for any selected period (using the date
slicer). Active status should be shown in Green background and the Inactive status to be
shown in Grey background.

### Features:
**Dynamic Employee Status:** 

Displays "Active" or "Inactive" status of employees based on their date range selection using a date slicer.

**Conditional Formatting:**

Active Status: Highlighted in Green.

Inactive Status: Highlighted in Grey.


**Flexible Date Filtering:** Allows the user to filter the data dynamically based on their selected date range, providing a snapshot of employee activity within that period.


---

## Data Preparation:

- Data is sourced from the Employee Status.xlsb file.

- A calender is created inorder to provide range for the selected period.

```
Date = CALENDAR(MIN('Employee Status'[DateStart]), MAX('Employee Status'[DateEnd]))
```

 - A calculated measure is created to determine the "Active" or "Inactive" status of each employee based on their start and end dates.

```
Status = 
VAR _startRange = FIRSTDATE('Date'[Date])
VAR _endRange = LASTDATE('Date'[Date])
VAR _dateStart = SELECTEDVALUE('Employee Status'[DateStart])
VAR _dateEnd = SELECTEDVALUE('Employee Status'[DateEnd])

RETURN 
IF(
    _startRange <= _dateStart && _dateEnd <= _endRange && NOT(ISBLANK(_dateEnd)),
    "Active", 
    "Inactive"
)
```

## Power BI Implementation:

 - A date slicer is used to select the desired period.
 - DAX formulas are utilized to compute the "Active/Inactive" status of employees for the selected date range.
 - Conditional formatting is applied to visually distinguish between "Active" (Green) and "Inactive" (Grey) statuses.


## Key DAX Calculations:

 - Calculated measures to determine if an employee's status falls within the selected period.
 - Logical functions to evaluate the status and apply formatting.


