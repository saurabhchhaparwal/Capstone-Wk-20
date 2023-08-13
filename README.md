Project Report for Week 20 : Capstone Project : Preventive Maintenance

Business Scenario: Company produces 100% customized windows and doors and sells directly to consumers. It has been growing significantly in the last few years and has reached it full capacity. New capacity projects are being implemented but the leadership wants to improve the efficiency and utilization of current assets. And a large portion of efficiency is lost due to unplanned breakdown of machines making it a slow and inefficient process to repair it. Also, it leads to high cost of running the operation thus, it’s desired to increase asset efficiency by reduction downtime and one way identified is plan the preventive maintenance at a certain frequency. 
Data Set: Downtime incidents recorded by operations team. Team recorded which asset was not working, duration it was not working and potential reason it was not working. 
Methodology:
Plan is to review the number of downtime incidents per day and per week and understand their trend with time. If few of the failure rate improves after maintenance work then, those assets must be added to predictive maintenance plan based on when the asset reaches a threshold. It should help reduce unpredictable reactive response to machine breakdown.
Steps followed: 
1)	Explored the dataset gathered in 2022 and 2023 for all production lines, assets and reason codes.
 

2)	Cleaned the data for any missing entries, dropped the columns not that were not needed.
3)	Summarized/grouped the minutes and counts of machine breakdown/downtime incidents.
4)	Data Review & Modelling: 
a.	Plotted assets with top 10 downtime incidents for all production lines. Link to the graphs are as follows:
b.	For modelling, data was split into training and test set by making 2022 data as training set and 2023 data as test set
c.	Create tsaplots and used adfuller method to evaluate if the data is stationary for a given asset and metric (minutes of downtime vs count of downtime) and most assets are with exception of few which are either increasing or decreasing trend.
d.	For assets which are not-stationary, evaluated “difference” of consecutive points to make them stationary.
e.	Used STLForecast method to model and fit 2022 data to predict 2023 incidents but it seems that ‘prediction’ are not close to ‘actuals’
5)	Conclusion
a.	This dataset cannot be used to predict the potential failure rate for most assets as most assets are not showing any trend or cyclical nature.
6)	Next Steps:
a.	Test is data is independent and if yes, then it cannot be forecasted.
b.	Bring in the dates when preventive maintenance was done to evaluate if it “mean time between failures” or number of incidents of machine breakdown decrease after machine “preventive maintenance.”
