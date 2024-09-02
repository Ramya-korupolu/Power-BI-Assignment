## File to refer: New Dispatch Log.csv

You are required to show the number of orders processed (both Arrival and Depart) at every
15 minutes interval (0-15, 16-30, 31-45, 46-60 minutes) all hours throughout the day. The
report should have the option of viewing the numbers separately for Arrival and Depart using
the slicer.

---

## 15-Minute Interval Analysis:

 - Groups the order data into 15-minute intervals (0-15, 16-30, 31-45, 46-60 minutes) for every hour of the day.
 - Provides a clear visualization of order processing trends within the defined intervals.


## Interactive Slicer:

 - Enables filtering of data to view "Arrival" and "Depart" order types separately and can view both.
 - Supports dynamic analysis and comparison of order processing patterns.

---

## Data Preparation:

 - Loads data from the New Dispatch Log.csv file using Power Query.
 - Cleans and prepares the data to ensure accurate time-based grouping.

## Power Query Transformation:

 - Creates calculated columns to group time into 15-minute intervals.
 - Uses separate measures for "Arrival" and "Depart" order counts.
## Combining the Tables:

 - Merges the "Arrival" and "Depart" tables into a single table with a common format to facilitate unified analysis.
 - Maintains the separation of types for slicer functionality and detailed visualization.

## Interactive Reporting in Power BI:

 - Implements slicers to toggle between "Arrival" and "Depart" order types.
 - Builds visualizations to show the number of orders processed at each interval throughout the day.
