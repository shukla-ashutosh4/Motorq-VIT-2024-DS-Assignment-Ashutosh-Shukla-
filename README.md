# Motorq-VIT-2024-DS-Assignment-Ashutosh-Shukla-
## 1. Data Preparation:
- **Combining Datasets:** 
  - Two telemetry datasets (Telemetry 1 and Telemetry 2) are combined by pivoting and appending them into a single dataset.
  - The combined telemetry data is then merged with the vehicle data, which contains essential information about each vehicle's fuel tank capacity and rated miles per gallon (MPG).

## 2. Data Processing:
- **Chronological Order:**
  - The dataset is sorted by `vehicle_id` and `timestamp` to ensure the data is in chronological order for accurate calculations.
- **Calculations:**
  - Changes in fuel level and odometer readings are calculated for each vehicle.
  - Fuel used is determined based on the difference in fuel level, considering the vehicle's tank capacity.

## 3. Identifying Refueling Events:
- **Detection:**
  - Refueling events are identified by detecting positive changes in the fuel level.
- **Exclusion:**
  - These refueling events are excluded from the fuel economy calculation to avoid skewing the results and to ensure accuracy.

## 4. Calculating Fuel Economy:
- **Segment Calculation:**
  - For each segment of data between refueling events, the fuel economy is calculated as the ratio of distance traveled (odometer change) to fuel used.
- **Average MPG:**
  - The average fuel economy (MPG) is then calculated for each vehicle, providing insights into the vehicle's efficiency.

## 5. Results:
- **Anomalies:**
  - The process may yield NaN or negative MPG values, which could indicate potential data issues or anomalies.
- **Further Processing:**
  - Further data validation and preprocessing may be necessary to refine the calculations and address any data inconsistencies.

## 6. Data Visualization:
- **Key Insights:**
  - **Distribution of Telemetry Types:** A bar chart showing the frequency of telemetry types (speed, odometer, fuel level).
  - **Average Values of Telemetry Data:** A bar chart illustrating the average values for speed, odometer, and fuel level.
  - **Vehicle Telemetry Counts:** A bar chart showing the number of telemetry entries recorded for each vehicle.

This process provides an overall understanding of how efficiently each vehicle is using fuel based on the telemetry data.
