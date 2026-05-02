README (for your Jupyter Notebook)
Title

The Pulse of the City: NYC Taxi Ecosystem Analysis

Objective

This project analyzes NYC taxi trip data to understand system behavior, passenger patterns, and operational stability. The goal is to determine whether the system is stable, biased, or drifting into inefficiency.

Data Source

NYC Taxi & Limousine Commission (TLC) trip record data (January 2023 sample).

Steps Performed
1. Data Loading
Loaded raw trip data from parquet/CSV
Converted timestamps and prepared structured dataset
2. Data Cleaning (Act-2)
Removed invalid trips:
Zero/negative fare
Zero distance
Invalid timestamps
Defined what constitutes a “real trip”
3. Behavioral Analysis (Act-3)
Hypothesis: Tipping behavior varies by payment type
Found:
Card payments show higher recorded tips
Cash tips are often not recorded → data bias
Removed outliers and analyzed tip % distribution
4. System Patterns (Act-4)
Aggregated data by hour and weekday
Observations:
Strong daily cycle (peak evening, low early morning)
Weekly pattern is stable
Some variations are noise
5. Simulation (Act-5)
Simulated 10% fare increase
Assumed 5% drop in trips
Result:
Revenue increased
System absorbed change
Conclusion: System is stable and adaptive
Key Insights
The system is cyclical (hourly patterns)
The system is stable (weekly consistency)
The system shows data bias (payment method effects)
The system is resilient to small policy changes
Limitations
Cash tips not fully recorded
Simulation based on assumptions
Sample dataset used (not full scale)
Conclusion

The NYC taxi ecosystem operates with a predictable rhythm driven by human mobility patterns. While generally stable, the system contains structural biases in data collection and requires careful interpretation for decision-making.

Tools Used
Python (Pandas, Matplotlib)
Jupyter Notebook
Power BI
