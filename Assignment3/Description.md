## File to refer: Tenant Score.xlsb


Using Power Query, please transform the tenant score table into a monthly snapshot fact
table. For each month, only the score of the maximum date is of interest. If there is no data
for a given month, the last value is valid. If needed, please create a date dimension using DAX.
If there are two scores for the same tenant and day, please take the higher score.

--- 


## Monthly Snapshot Fact Table:
 - Generates a monthly snapshot of tenant scores by retaining only the highest score of the latest date in each month.
 - Handles missing data by carrying forward the most recent score from the previous month.
 - Selects the highest score for cases where multiple scores exist on the same date for a tenant.

---
## Data Preparation:

 - Loads data from the Tenant Score.xlsb file using Power Query.
 - Cleans and transforms the data to create a monthly snapshot fact table.


## Power Query Implementation:

 - Groups data by tenant and month.
 - Aggregates to find the maximum score for the latest date in each month.
 - Ensures the last available score is carried forward for months with no data.


## Date Dimension Creation:

 - Creates a date dimension table using DAX (e.g. CALENDARAUTO) to support monthly aggregation.
 - Associates the date dimension with the tenant score data to handle time-based calculations.
