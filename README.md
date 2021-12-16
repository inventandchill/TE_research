# TEC Rewards System Analysis

# Team 13: (π Party)
Created by:

***inventandchill#7140***

***sidcode#1729***


# 
Source code: https://nbviewer.org/github/inventandchill/TE_research/blob/main/Praise_charts.ipynb

*Thanks to Teodoro **teodoro.criscione#0572** for sharing the python parser for TE praise data*

*Thanks to Shawn **ygg_anderson#4998** for idea to exlude iviangita from dataset*

*Thanks to **🐙 octopus#5508** for idea to use log of data*

*Thanks to Angela **akrtws (TE Academy)#4246** for idea to check relationship between amount Praised and Received* 

*Thanks to Livia **liviade#1387** for positive and useful feedback* 

### Data

Batch 1: 2020-Sep-29 to 2021-May-07

Batch 3: Most part from 2021-May-08 to 2021-Jul-11

Batch 2: Few data 2020-Sep-23 to 2020-Nov-20


### Measuring system healthiness generally
For deeply measuring system healthiness, we need to create visual representation of data using different methods. 

### Hypothesis

- Is there any imbalance and whale-behaviour in the Praise and IH flow distribution? 
- How does IH get distributed in general and for largest Praise sender? Is it like normal distribution or skewed 
- Is there relationship between amount of praised and amount of received for IH and count of events 

### Analysis
We use python to create **Flow diagram (Sankey)** for 2 types of data:
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


Praise flow for Batch 1 - **Sum** of Praise, exclude iviangita  
![](https://cdn.discordapp.com/attachments/916006305737605140/916292468515930152/Praise_flow_for_Batch_1_-_Sum_of_Praise_exclude_iviangita.png)

Praise flow for Batch 3 - **Sum** of Praise, exclude iviangita  
![](https://cdn.discordapp.com/attachments/916006305737605140/916294064045957190/Praise_flow_for_Batch_3_-_Sum_of_Praise_exclude_iviangita.png)

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

Relationship between IH Praised and IH received. Relationship between amount of events Praised and amount of events received.

![](https://cdn.discordapp.com/attachments/907710579693748224/918544801404710912/IH_1.jpg)

![](https://cdn.discordapp.com/attachments/907710579693748224/918544820325195786/IH_3.jpg)

![](https://cdn.discordapp.com/attachments/907710579693748224/918544855943249930/events_1.jpg)

![](https://cdn.discordapp.com/attachments/907710579693748224/918544874259755038/events_3.jpg)

![](https://cdn.discordapp.com/attachments/921078273323188247/921078903211196446/Batch1_log_IH.jpg)

![](https://cdn.discordapp.com/attachments/921078273323188247/921078950380339210/Batch3_log_IH.jpg)

![](https://cdn.discordapp.com/attachments/921078273323188247/921079010442752040/Batch1_log_event.jpg)

![](https://cdn.discordapp.com/attachments/921078273323188247/921079028725743726/Batch3_log_event.jpg)


### Analysis conclusion
1. Flow charts created for praise count (events) and praise IH sum are pretty similar. This result corresponds with praise IH have near-to-skewed distribution
2. On average, Top 10 praise senders are responsible  for more than 75% of IH
3. On average, Top 15 praise receiver are responsible for around 70% of IH
4. Except for `iviangita` other praise senders without big outliers for both metrics (praise count (events) and praise IH sum) 
5. Distribution of IH of largest praise sender (iviangita) is correpond with distribution of IH of all praise senders, except Batch 2
6. IH Praised and IH received by participant have strong relationship 
7. Amount of event Praised and amount of event received by participant have strong relationship 


### Zoom out again, does this analysis suggest anything about system health? 
Analysis suggest that system is relatively healthy and without many whales who control all praise distribution, but it is always many ways for improvements. 

As an indicator of system diversification, it is possible to track the Gini index based on two key metrics: 
1. Praise count (events)
2. Praise IH sum

Both metrics could be used for praise senders+receivers

We can calculate this indicator for any configuration- all times, or for batches of specific time periods like 1 week, etc.
