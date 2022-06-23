# -3-Control-Chart-for-Train-Defect

### What is a Control Chart?

The control chart is a graph used to study how a process changes over time. Data are plotted in time order. A control chart always has a central line for the average, an upper line for the upper control limit (UCL) which is 3 standard deviation higher from the average, and a lower line for the lower control limit (LCL) which is 3 standard deviation lower from the average. These lines are determined from historical data.


![alt text](https://asq.org/-/media/Images/Learn-About-Quality/Seven-Basic-Quality-Tools/dcat-control-chart.gif?la=en)

Reference
https://asq.org/quality-resources/control-chart

### What are we doing with a control chart?

Control chart are used in production line, defect monitoring, sensor monitoring to provide an indication whehter the system is in control. Stakeholders use it to look out for any cause for concern and provide a mitigation plan, if required.

Control Chart has mainly 8 types of chart patterns that signal Out-of-control. In this study, we will be using the following 2 indicators as they provide the strongest indication for concern:

1) An large shift deviated from mean rate (3 Standard Deviation from average) indicate for an unforeseen event 
2) An trend. (3 consecutive higher than previous point) indicate for a sign of increasing defects.

### Data 

Data showcase in this case study are gathered from a train operator based in a highly populated and warm area. Reported faults are between 2019-Jan to 2022-May. Sensitive information has been replaced with a dummy information.

#### Dataset 1 (Train Defect Data) - Train defect data.

Record_MonthName - Month-year of the reported fault.
Fault_Group - Classification of fault type. (e.g. Aircon System)
Cause - Faulty component name (e.g. Aircon Evaporator Motor failure)
Fleet - Train Type (e.g. Fleet ABC)

#### Dataset 2 (Train Mileage Data) - Train mileage is the distance which the train has travelled to normalise defect rate between fleets.

ABC (Monthly)- Month-year of the Fleet ABC Mileage
XYZ (Monthly)- Month-year of the Fleet XYZ Mileage

#### Dataset 3 (Train Withdrawal Data) - Train withdrawal means that the train has a defects during servicing that requires withdrawal from service. It will result in the trains' passengers disembarked at the next nearest station. This is one of the KPI that train operator tracks to improve passenger service.

Year_Month - Month-year of the reported train withdrawal
StockChange Withdrawal - A service defect resulted in a train withdrawal.
Fault_Group - Classification of fault type. (e.g. Aircon System)
Fleet - Train Type (e.g. Fleet ABC)

### Objective
The main objective of this project is to aggregate the data and provide a meaningful visualisation for the stakeholders.
1) To aggregate the defect data so that an overview of all the critical train system's health can be easily visualised. Python (Pandas and Numpy) will be used here.
2) To improve visualisation of the control chart by making the 2 out-of-control signals stands out. PowerBi will be used here.


### Steps
Steps involved in this study include

1) Cleaning of data - removal of unncessary data and filling Nil data - Using Pandas library.
2) Aggregate the data -  To groupby the data by fleet and Fault group 
3) Feature Engineering 
- Identify the mean defect of each fleet Fault Group
- Create a column that can visualise UCL line Not concern with LCL for defect rate)
- Create a column that can visualise a data point that went above UCL line.
- Create a column that can visualise an upward trend. (Not concern with downward trend for defect rate)
- Join the defect rate data with the withdrawal rate data
- Visualise it on the Dashboard.

## Result


![alt text](https://i.ibb.co/4fjPzgC/train.jpg)
![alt text](https://asq.org/-/media/Images/Learn-About-Quality/Seven-Basic-Quality-Tools/dcat-control-chart.gif?la=en)




















Reference
https://asq.org/quality-resources/control-chart
