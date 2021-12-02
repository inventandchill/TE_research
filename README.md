# TEC Rewards System Anlaysis

# Team 3.14

Source code: https://nbviewer.org/github/inventandchill/TE_research/blob/main/Praise_charts.ipynb

*Thanks to **teodoro.criscione#0572** for sharing python parser of TE praise data*

### Measuring system healthiness generally
For deep measuring system healthiness we need to create visual representation of data using different methods. 

### Hypothesis

Is there any imbalances and whales in Praise and IH flow distribution? 

How does IH distributed in general and for largest Praise sender? Is it like normal distribution or skewed 

### Analysis
We use python to crate **Flow diagram (Sankey)** for 2 types of data:
1. Amount of Praises
2. Total sum of IH

"Rest From" represents combined Senders who are not in Top 10 by total IH contribution

"Rest To" represents combined Receivers who are not in Top 15 by total IH receiving

Example for **flow chart**. 
A_sender praise C_reciever with IH=1
B_sender praise C_reciever with IH=3
A_sender praise D_reciever with IH=5

**Count of praise** (events) for A_sender 1+1=2
**Sum of praise** for  A_sender 1+5=6

**Count of praise** (events) for C_receiver 1+1=2
**Sum of praise** for  C_receiver 1+3=4

For **histogram**
X axis - size of praise
Y axis - amount of contributions with size on x axis
Example
We have 5 praises with IH = 7
So for x = 7 it woud be y=5 

Praise flow for Batch 1 - **Count** of Praise  
![](https://cdn.discordapp.com/attachments/911319098426814466/915537022620422154/Praise_flow_for_Batch_1_-_Count_of_Praise.png)

Praise flow for Batch 2 - **Count** of Praise  
![](https://cdn.discordapp.com/attachments/911319098426814466/915537103826341908/Praise_flow_for_Batch_2_-_Count_of_Praise.png)

Praise flow for Batch 3 - **Count** of Praise  
![](https://cdn.discordapp.com/attachments/911319098426814466/915537137108148224/Praise_flow_for_Batch_3_-_Count_of_Praise.png)

Praise flow for Batch 1 - **Sum** of Praise  
![](https://cdn.discordapp.com/attachments/911319098426814466/915537197418045450/Praise_flow_for_Batch_1_-_Sum_of_Praise.png)

Praise flow for Batch 2 - **Sum** of Praise  
![](https://cdn.discordapp.com/attachments/911319098426814466/915537282533044244/Praise_flow_for_Batch_2_-_Sum_of_Praise.png)

Praise flow for Batch 3 - **Sum** of Praise  
![](https://cdn.discordapp.com/attachments/911319098426814466/915537314732707870/Praise_flow_for_Batch_3_-_Sum_of_Praise.png)



Praise amount **histogram** for all 3 batches. Simple and zoomed

![](https://cdn.discordapp.com/attachments/911319098426814466/915569558826414091/Praise_amount_histogram_for_Batch_1.png)

![](https://cdn.discordapp.com/attachments/911319098426814466/915569578803863582/Praise_amount_histogram_for_Batch_1_zoom.png)

![](https://cdn.discordapp.com/attachments/911319098426814466/915569602770128946/Praise_amount_histogram_for_Batch_2.png)

![](https://cdn.discordapp.com/attachments/911319098426814466/915569615281750037/Praise_amount_histogram_for_Batch_2_zoom.png)

![](https://cdn.discordapp.com/attachments/911319098426814466/915569632910405642/Praise_amount_histogram_for_Batch_3.png)

![](https://cdn.discordapp.com/attachments/911319098426814466/915569644759298098/Praise_amount_histogram_for_Batch_3_zoom.png)

Histogram for **iviangita**

![](https://cdn.discordapp.com/attachments/911319098426814466/915605307370127400/iviangita_Praise_amount_histogram_for_Batch_1.png)

![](https://cdn.discordapp.com/attachments/911319098426814466/915605536781762630/iviangita_Praise_amount_histogram_for_Batch_2.png)

![](https://cdn.discordapp.com/attachments/911319098426814466/915605549440172082/iviangita_Praise_amount_histogram_for_Batch_3.png)

### Analysis conclusion
1. Flow charts created for praise count (events) and praise IH sum are pretty similar. And this result correspond with praise IH have near to skewed distribution
2. On average Top 10 praise senders are responsible  for more than 75% of IH
3. On average Top 15 praise receiver are responsible for around 70% of IH
4. Except for iviangita other praise senders without big outliers for both metrics (praise count (events) and praise IH sum) 
5. Distribution of IH of largest praise sender (iviangita) is correpond with distribution of IH of all praise senders, except Batch 2


### Zoom out again, does this analysis suggest anything about system health? 
Analysis suggest that system is relatively healthy and without many whales who control all praise distribution, but it is always many ways for improvements. 

As an indicator of system diversification, it is possible to create tracking Gini index based on 2 metrics: 
1. Praise count (events)
2. Praise IH sum

Both metrics could be used for praise senders and praise receivers

We can calculate this indicator for all times, for batches of for specific time periods like 1 week
