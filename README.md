# -3-Control-Chart-for-Train-Defect

###What is a Control Chart?

The control chart is a graph used to study how a process changes over time. Data are plotted in time order. A control chart always has a central line for the average, an upper line for the upper control limit (UCL) which is 3 standard deviation higher from the average, and a lower line for the lower control limit (LCL) which is 3 standard deviation lower from the average. These lines are determined from historical data.


![alt text](https://asq.org/-/media/Images/Learn-About-Quality/Seven-Basic-Quality-Tools/dcat-control-chart.gif?la=en)
Reference
https://asq.org/quality-resources/control-chart

###What are we doing with a control chart?

Control chart are used in production line, defect monitoring, component sensor monitoring to provide an indication system not in control. Stakeholders use it to look out for any cause for concern and provide a mitigation plan, if required.

Control Chart has mainly 8 types of chart patterns that signal Out-of-control. In this study, we will be using the following 2 indicators only:

1) An large shift deviated from mean rate (3 Standard Deviation from average) indicate for an unforeseen event 
2) An trend. (3 consecutive higher than previous point) indicate for a sign of increasing defects.

###Data 

Data showcase in this case study are gathered from a train operator based in a highly populated and warm area. Reported faults are between 2019-Jan to 2022-May. Sensitive information has been replaced with a dummy information.

####dataset 1 (Train Defect Data) - Train defect data.

Record_MonthName - Month-year of the reported fault.
Fault_Group - Classification of fault type. (e.g. Aircon System)
Cause - Faulty component name (e.g. Aircon Evaporator Motor failure)
Fleet - Train Type (e.g. Fleet ABC)

####dataset 2 (Train Mileage Data) - Train mileage is the distance which the train has travelled. Similar to car mileage. It is used to normalise defect rate.

ABC (Monthly)- Month-year of the Fleet ABC Mileage
XYZ (Monthly)- Month-year of the Fleet XYZ Mileage

####dataset 3 (Train Withdrawal Data) - Train withdrawal means that the train has a defects during servicing that requires withdrawal from service. It will result in the trains' passengers disembarked at the next nearest station. This is one of the KPI that train operator tracks to improve passenger service.

Year_Month - Month-year of the reported train withdrawal
StockChange Withdrawal - A service defect resulted in a train withdrawal.
Fault_Group - Classification of fault type. (e.g. Aircon System)
Fleet - Train Type (e.g. Fleet ABC)

###Step
Steps involved in this study include

Cleaning of data - removal of unncessary data and filling Nil data - Using Pandas library.


























Reference
https://asq.org/quality-resources/control-chart
