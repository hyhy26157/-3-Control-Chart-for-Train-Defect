# Case Study #3 - Control Chart Visualisation

### What is a Control Chart?

The control chart is a graph used to study how a process changes over time. Data are plotted in time order. A control chart always has a central line for the average, an upper line for the upper control limit (UCL) which is 3 standard deviation higher from the average, and a lower line for the lower control limit (LCL) which is 3 standard deviation lower from the average. These lines are determined from historical data.


![alt text](https://asq.org/-/media/Images/Learn-About-Quality/Seven-Basic-Quality-Tools/dcat-control-chart.gif?la=en)

Reference
https://asq.org/quality-resources/control-chart

### What are we doing with a control chart?

Control chart are used in production line, defect trending, sensor monitoring to provide an indication whehter the system is in control. Stakeholders use it to look out for any cause for concern and provide a mitigation plan, if required.

Control Chart has mainly 8 types of chart patterns that signal Out-of-control. In this study, we will be using the following 2 indicators as they provide the strongest indication for concern:

1) An large shift deviated from mean rate (3 Standard Deviation from average) indicate for an unforeseen event 
2) An trend. (3 consecutive higher than previous point) indicate for a sign of increasing defects.

### Data 

Data showcase in this case study are gathered from a train operator based in metropolis with warm climate. Reported faults are between 2019-Jan to 2022-May. Sensitive information has been replaced with a dummy information.

#### Dataset 1 (Train Defect Data) - Train defect data.

- Record_MonthName - Month-year of the reported fault.
- Fault_Group - Classification of fault type. (e.g. Aircon System)
- Cause - Faulty component name (e.g. Aircon Evaporator Motor failure)
- Fleet - Train Type (e.g. Fleet ABC)

#### Dataset 2 (Train Mileage Data) - Train mileage is the distance (in million km) which the train has travelled. The data is use to normalise defect rate between fleets.

- ABC (Monthly)- Month-year of the Fleet ABC Mileage
- XYZ (Monthly)- Month-year of the Fleet XYZ Mileage

#### Dataset 3 (Train Withdrawal Data) - Train withdrawal means train defects happened during service hours and it is removed from servicing. Trains' passengers will disembark at next nearest station. This is one of the KPI the train operator tracks, to improve passenger experience.

- Year_Month - Month-year of the reported train withdrawal
- StockChange Withdrawal - A service defect resulted in a train withdrawal.
- Fault_Group - Classification of fault type. (e.g. Aircon System)
- Fleet - Train Type (e.g. Fleet ABC)

### Objective

The main objective of this project is to aggregate the data and provide a meaningful visualisation for the stakeholders to understand the overview of the fault and provide a mitigation plan.
1) To aggregate the defect data so that an overview of all the critical train system's health can be easily visualised. Python (Pandas and Numpy) will be used here.
2) To improve visualisation of the control chart by making the 2 out-of-control signals stands out. PowerBi will be used here.

### Storytelling

![alt text](https://i.ibb.co/bPYXhWT/Capture.jpg)

Reference
https://www.storytellingwithdata.com/

I have used Cole Nussbaumer knaflics Storytelling with data book to To improve visualise of the Contorl Chart to suit the audience. 

Essentially, there are 5 steps to Data Storytelling;

1) Understand the context - What is the problem statement?
<br /> The context is that the stakeholders would like to have an overview of the train system reliability, to ensure that area of concern is captured before it leads to train service delay.

2) Choose an effective Visualisation - What are some of the visualisation graphs used to illustate the storytelling?
<br /> The go-to graph for a time-series data is line chart. It is a popular graph type and executives (non technical) can understand it easily. Control Chart is a type of line chart. We will be using it for this study.

3) Eliminate Cluster - How many visualisation graph is requireed?
<br /> We have 3 datasets in this project. However, we can aggregate the data so that the 3 dataset information can be effectively combined into 1 chart.

4) Focus attention - What are the information that is unncessary in the visualisation graph?
<br /> We will focus on the 2 major indicators (line 18 and 19) used in control chart that provides that most useful information for defect trending.

5) Tell a story - What are the mode of presentation?
<br /> 

### Steps
Steps involved in this study includes

1) Cleaning of data - removal of unncessary data and filling Nil data - Using Pandas library.
2) Aggregate the data -  To groupby the data by fleet and Fault group 
3) Feature Engineering 

<br />  3.1) Create a column that can visualise mean defect.
<br />  3.2) Create a column that can visualise UCL line.
<br />  3.3) Create a column that can visualise a data point that went above UCL line.
<br />  3.4) Create a column that can visualise an upward trend. (Not concern with downward trend for defect rate)

5) Perform a combo chart to join withdrawal data with defect data.
6) Visualise on the dashboard.


## Result


![alt text](https://asq.org/-/media/Images/Learn-About-Quality/Seven-Basic-Quality-Tools/dcat-control-chart.gif?la=en)












Reference
https://asq.org/quality-resources/control-chart
