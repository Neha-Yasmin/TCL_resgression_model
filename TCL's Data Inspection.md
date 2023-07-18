# **Automatidata project**
**Course 2 - Get Started with Python**

Welcome to the Automatidata Project!

You have just started as a data professional in a fictional data consulting firm, Automatidata. Their client, the New York City Taxi and Limousine Commission (New York City TLC), has hired the Automatidata team for its reputation in helping their clients develop data-based solutions.

The team is still in the early stages of the project. Previously, you were asked to complete a project proposal by your supervisor, DeShawn Washington. You have received notice that your project proposal has been approved and that New York City TLC has given the Automatidata team access to their data. To get clear insights, New York TLC's data must be analyzed, key variables identified, and the dataset ensured it is ready for analysis.

A notebook was structured and prepared to help you in this project. Please complete the following questions.

# Course 2 End-of-course project: Inspect and analyze data

In this activity, you will examine data provided and prepare it for analysis.  This activity will help ensure the information is,

1.   Ready to answer questions and yield insights

2.   Ready for visualizations

3.   Ready for future hypothesis testing and statistical methods
<br/>    

**The purpose** of this project is to investigate and understand the data provided.
  
**The goal** is to use a dataframe contructed within Python, perform a cursory inspection of the provided dataset, and inform team members of your findings. 
<br/>  
*This activity has three parts:*

**Part 1:** Understand the situation 
* Prepare to understand and organize the provided taxi cab dataset and information.

**Part 2:** Understand the data

* Create a pandas dataframe for data learning, future exploratory data analysis (EDA), and statistical activities.

* Compile summary information about the data to inform next steps.

**Part 3:** Understand the variables

* Use insights from your examination of the summary data to guide deeper investigation into specific variables.


<br/> 
Follow the instructions and answer the following questions to complete the activity. Then, you will complete an Executive Summary using the questions listed on the PACE Strategy Document.

Be sure to complete this activity before moving on. The next course item will provide you with a completed exemplar to compare to your own work. 



# **Identify data types and relevant variables using Python**


<img src="images/Pace.png" width="100" height="100" align=left>

# **PACE stages**


Throughout these project notebooks, you'll see references to the problem-solving framework PACE. The following notebook components are labeled with the respective PACE stage: Plan, Analyze, Construct, and Execute.

<img src="images/Plan.png" width="100" height="100" align=left>


## PACE: **Plan**

Consider the questions in your PACE Strategy Document and those below to craft your response:

### **Task 1. Understand the situation**

*   How can you best prepare to understand and organize the provided taxi cab information? 

=> We can summarize the data using built-in functions of python such as info().

<img src="images/Analyze.png" width="100" height="100" align=left>

## PACE: **Analyze**

Consider the questions in your PACE Strategy Document to reflect on the Analyze stage.

### **Task 2a. Build dataframe**
















Create a pandas dataframe for data learning, and future exploratory data analysis (EDA) and statistical activities.

**Code the following,**

*   import pandas as pd. pandas is used for buidling dataframes.

*   import numpy as np. numpy is imported with pandas

*   df = pd.read_csv('Datasets\NYC taxi data.csv')

**Note:** pair the data object name "df" with pandas functions to manipulate data, such as df.groupby().

**Note:** As shown in this cell, the dataset has been automatically loaded in for you. You do not need to download the .csv file, or provide more code, in order to access the dataset and proceed with this lab. Please continue with this activity by completing the following instructions.


```python
import pandas as pd
import numpy as np

df = pd.read_csv('2017_Yellow_Taxi_Trip_Data.csv')
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>24870114</td>
      <td>2</td>
      <td>03/25/2017 8:55:43 AM</td>
      <td>03/25/2017 9:09:47 AM</td>
      <td>6</td>
      <td>3.34</td>
      <td>1</td>
      <td>N</td>
      <td>100</td>
      <td>231</td>
      <td>1</td>
      <td>13.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>2.76</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>16.56</td>
    </tr>
    <tr>
      <th>1</th>
      <td>35634249</td>
      <td>1</td>
      <td>04/11/2017 2:53:28 PM</td>
      <td>04/11/2017 3:19:58 PM</td>
      <td>1</td>
      <td>1.80</td>
      <td>1</td>
      <td>N</td>
      <td>186</td>
      <td>43</td>
      <td>1</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>4.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>20.80</td>
    </tr>
    <tr>
      <th>2</th>
      <td>106203690</td>
      <td>1</td>
      <td>12/15/2017 7:26:56 AM</td>
      <td>12/15/2017 7:34:08 AM</td>
      <td>1</td>
      <td>1.00</td>
      <td>1</td>
      <td>N</td>
      <td>262</td>
      <td>236</td>
      <td>1</td>
      <td>6.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>1.45</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>8.75</td>
    </tr>
    <tr>
      <th>3</th>
      <td>38942136</td>
      <td>2</td>
      <td>05/07/2017 1:17:59 PM</td>
      <td>05/07/2017 1:48:14 PM</td>
      <td>1</td>
      <td>3.70</td>
      <td>1</td>
      <td>N</td>
      <td>188</td>
      <td>97</td>
      <td>1</td>
      <td>20.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>6.39</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>27.69</td>
    </tr>
    <tr>
      <th>4</th>
      <td>30841670</td>
      <td>2</td>
      <td>04/15/2017 11:32:20 PM</td>
      <td>04/15/2017 11:49:03 PM</td>
      <td>1</td>
      <td>4.37</td>
      <td>1</td>
      <td>N</td>
      <td>4</td>
      <td>112</td>
      <td>2</td>
      <td>16.5</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>17.80</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>22694</th>
      <td>14873857</td>
      <td>2</td>
      <td>02/24/2017 5:37:23 PM</td>
      <td>02/24/2017 5:40:39 PM</td>
      <td>3</td>
      <td>0.61</td>
      <td>1</td>
      <td>N</td>
      <td>48</td>
      <td>186</td>
      <td>2</td>
      <td>4.0</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>5.80</td>
    </tr>
    <tr>
      <th>22695</th>
      <td>66632549</td>
      <td>2</td>
      <td>08/06/2017 4:43:59 PM</td>
      <td>08/06/2017 5:24:47 PM</td>
      <td>1</td>
      <td>16.71</td>
      <td>2</td>
      <td>N</td>
      <td>132</td>
      <td>164</td>
      <td>1</td>
      <td>52.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>14.64</td>
      <td>5.76</td>
      <td>0.3</td>
      <td>73.20</td>
    </tr>
    <tr>
      <th>22696</th>
      <td>74239933</td>
      <td>2</td>
      <td>09/04/2017 2:54:14 PM</td>
      <td>09/04/2017 2:58:22 PM</td>
      <td>1</td>
      <td>0.42</td>
      <td>1</td>
      <td>N</td>
      <td>107</td>
      <td>234</td>
      <td>2</td>
      <td>4.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>5.30</td>
    </tr>
    <tr>
      <th>22697</th>
      <td>60217333</td>
      <td>2</td>
      <td>07/15/2017 12:56:30 PM</td>
      <td>07/15/2017 1:08:26 PM</td>
      <td>1</td>
      <td>2.36</td>
      <td>1</td>
      <td>N</td>
      <td>68</td>
      <td>144</td>
      <td>1</td>
      <td>10.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>1.70</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>13.00</td>
    </tr>
    <tr>
      <th>22698</th>
      <td>17208911</td>
      <td>1</td>
      <td>03/02/2017 1:02:49 PM</td>
      <td>03/02/2017 1:16:09 PM</td>
      <td>1</td>
      <td>2.10</td>
      <td>1</td>
      <td>N</td>
      <td>239</td>
      <td>236</td>
      <td>1</td>
      <td>11.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>2.35</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>14.15</td>
    </tr>
  </tbody>
</table>
<p>22699 rows × 18 columns</p>
</div>



### **Task 2b. Understand the data - Inspect the data**

View and inspect summary information about the dataframe by coding the following:

1. df.head(10)
2. df.info()
3. df.describe()

Consider the following two questions:

**Question 1:** When reviewing the df.info() output, what do you notice about the different variables? Are there any null values? Are all of the variables numeric? Does anything else stand out?

**Question 2:** When reviewing the df.describe() output, what do you notice about the distributions of each variable? Are there any questionable values?

    1) The dataset majorly contains integer and floating point numbers. Out of 18 columns only 3 columns are of object data type in which two fields contain pick up and drop time (i.e. thery belong to datetime data type) and the third column contains boolean value ('Y' and 'N').

    There are no null values in the dataset.
    
    The fields payment_type, RatecodeID, PULocationID, and DOLocationID contain notations that have some known meaning to them. In order to analyze the dataset, we will need to determine the exact meaning of the values present in the columns.
    
    There exist 148 observations where the trip_distance is 0.00 km but all the other fields contains data that differ from 0.
    There are some negative values in the total_amount column.
    The maximum total_amount and trip_Distance differs greatly from the other data present in the field.
    


```python
df.head()
# df.groupby(['store_and_fwd_flag']).count()
# df.groupby(['payment_type']).count()


```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>24870114</td>
      <td>2</td>
      <td>03/25/2017 8:55:43 AM</td>
      <td>03/25/2017 9:09:47 AM</td>
      <td>6</td>
      <td>3.34</td>
      <td>1</td>
      <td>N</td>
      <td>100</td>
      <td>231</td>
      <td>1</td>
      <td>13.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>2.76</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>16.56</td>
    </tr>
    <tr>
      <th>1</th>
      <td>35634249</td>
      <td>1</td>
      <td>04/11/2017 2:53:28 PM</td>
      <td>04/11/2017 3:19:58 PM</td>
      <td>1</td>
      <td>1.80</td>
      <td>1</td>
      <td>N</td>
      <td>186</td>
      <td>43</td>
      <td>1</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>4.00</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>20.80</td>
    </tr>
    <tr>
      <th>2</th>
      <td>106203690</td>
      <td>1</td>
      <td>12/15/2017 7:26:56 AM</td>
      <td>12/15/2017 7:34:08 AM</td>
      <td>1</td>
      <td>1.00</td>
      <td>1</td>
      <td>N</td>
      <td>262</td>
      <td>236</td>
      <td>1</td>
      <td>6.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>1.45</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>8.75</td>
    </tr>
    <tr>
      <th>3</th>
      <td>38942136</td>
      <td>2</td>
      <td>05/07/2017 1:17:59 PM</td>
      <td>05/07/2017 1:48:14 PM</td>
      <td>1</td>
      <td>3.70</td>
      <td>1</td>
      <td>N</td>
      <td>188</td>
      <td>97</td>
      <td>1</td>
      <td>20.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>6.39</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>27.69</td>
    </tr>
    <tr>
      <th>4</th>
      <td>30841670</td>
      <td>2</td>
      <td>04/15/2017 11:32:20 PM</td>
      <td>04/15/2017 11:49:03 PM</td>
      <td>1</td>
      <td>4.37</td>
      <td>1</td>
      <td>N</td>
      <td>4</td>
      <td>112</td>
      <td>2</td>
      <td>16.5</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>17.80</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 22699 entries, 0 to 22698
    Data columns (total 18 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   Unnamed: 0             22699 non-null  int64  
     1   VendorID               22699 non-null  int64  
     2   tpep_pickup_datetime   22699 non-null  object 
     3   tpep_dropoff_datetime  22699 non-null  object 
     4   passenger_count        22699 non-null  int64  
     5   trip_distance          22699 non-null  float64
     6   RatecodeID             22699 non-null  int64  
     7   store_and_fwd_flag     22699 non-null  object 
     8   PULocationID           22699 non-null  int64  
     9   DOLocationID           22699 non-null  int64  
     10  payment_type           22699 non-null  int64  
     11  fare_amount            22699 non-null  float64
     12  extra                  22699 non-null  float64
     13  mta_tax                22699 non-null  float64
     14  tip_amount             22699 non-null  float64
     15  tolls_amount           22699 non-null  float64
     16  improvement_surcharge  22699 non-null  float64
     17  total_amount           22699 non-null  float64
    dtypes: float64(8), int64(7), object(3)
    memory usage: 3.1+ MB



```python
df.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>2.269900e+04</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>5.675849e+07</td>
      <td>1.556236</td>
      <td>1.642319</td>
      <td>2.913313</td>
      <td>1.043394</td>
      <td>162.412353</td>
      <td>161.527997</td>
      <td>1.336887</td>
      <td>13.026629</td>
      <td>0.333275</td>
      <td>0.497445</td>
      <td>1.835781</td>
      <td>0.312542</td>
      <td>0.299551</td>
      <td>16.310502</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.274493e+07</td>
      <td>0.496838</td>
      <td>1.285231</td>
      <td>3.653171</td>
      <td>0.708391</td>
      <td>66.633373</td>
      <td>70.139691</td>
      <td>0.496211</td>
      <td>13.243791</td>
      <td>0.463097</td>
      <td>0.039465</td>
      <td>2.800626</td>
      <td>1.399212</td>
      <td>0.015673</td>
      <td>16.097295</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.212700e+04</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>-120.000000</td>
      <td>-1.000000</td>
      <td>-0.500000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>-0.300000</td>
      <td>-120.300000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2.852056e+07</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.990000</td>
      <td>1.000000</td>
      <td>114.000000</td>
      <td>112.000000</td>
      <td>1.000000</td>
      <td>6.500000</td>
      <td>0.000000</td>
      <td>0.500000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.300000</td>
      <td>8.750000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>5.673150e+07</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>1.610000</td>
      <td>1.000000</td>
      <td>162.000000</td>
      <td>162.000000</td>
      <td>1.000000</td>
      <td>9.500000</td>
      <td>0.000000</td>
      <td>0.500000</td>
      <td>1.350000</td>
      <td>0.000000</td>
      <td>0.300000</td>
      <td>11.800000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>8.537452e+07</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>3.060000</td>
      <td>1.000000</td>
      <td>233.000000</td>
      <td>233.000000</td>
      <td>2.000000</td>
      <td>14.500000</td>
      <td>0.500000</td>
      <td>0.500000</td>
      <td>2.450000</td>
      <td>0.000000</td>
      <td>0.300000</td>
      <td>17.800000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.134863e+08</td>
      <td>2.000000</td>
      <td>6.000000</td>
      <td>33.960000</td>
      <td>99.000000</td>
      <td>265.000000</td>
      <td>265.000000</td>
      <td>4.000000</td>
      <td>999.990000</td>
      <td>4.500000</td>
      <td>0.500000</td>
      <td>200.000000</td>
      <td>19.100000</td>
      <td>0.300000</td>
      <td>1200.290000</td>
    </tr>
  </tbody>
</table>
</div>



### **Task 2c. Understand the data - Investigate the variables**

Sort and interpret the data table for two variables:`trip_distance` and `total_amount`.

**Answer the following three questions:**

**Question 1:** Sort your first variable (`trip_distance`) from maximum to minimum value, do the values seem normal?

**Question 2:** Sort by your second variable (`total_amount`), are any values unusual?

**Question 3:** Are the resulting rows similar for both sorts? Why or why not?

    There is a great difference between the highest value of the trip_distance and total_amount fields.
    
    The highest amount paid was 1200 whereas fro the largest trip_distance the amount paid was onlt 150.30


```python
df.sort_values(by = ['trip_distance'], ascending = False)

# Sort the data by trip distance from maximum to minimum value
# mask = df['trip_distance'] == 0.00
# df[mask]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9280</th>
      <td>51810714</td>
      <td>2</td>
      <td>06/18/2017 11:33:25 PM</td>
      <td>06/19/2017 12:12:38 AM</td>
      <td>2</td>
      <td>33.96</td>
      <td>5</td>
      <td>N</td>
      <td>132</td>
      <td>265</td>
      <td>2</td>
      <td>150.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>150.30</td>
    </tr>
    <tr>
      <th>13861</th>
      <td>40523668</td>
      <td>2</td>
      <td>05/19/2017 8:20:21 AM</td>
      <td>05/19/2017 9:20:30 AM</td>
      <td>1</td>
      <td>33.92</td>
      <td>5</td>
      <td>N</td>
      <td>229</td>
      <td>265</td>
      <td>1</td>
      <td>200.01</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>51.64</td>
      <td>5.76</td>
      <td>0.3</td>
      <td>258.21</td>
    </tr>
    <tr>
      <th>6064</th>
      <td>49894023</td>
      <td>2</td>
      <td>06/13/2017 12:30:22 PM</td>
      <td>06/13/2017 1:37:51 PM</td>
      <td>1</td>
      <td>32.72</td>
      <td>3</td>
      <td>N</td>
      <td>138</td>
      <td>1</td>
      <td>1</td>
      <td>107.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>55.50</td>
      <td>16.26</td>
      <td>0.3</td>
      <td>179.06</td>
    </tr>
    <tr>
      <th>10291</th>
      <td>76319330</td>
      <td>2</td>
      <td>09/11/2017 11:41:04 AM</td>
      <td>09/11/2017 12:18:58 PM</td>
      <td>1</td>
      <td>31.95</td>
      <td>4</td>
      <td>N</td>
      <td>138</td>
      <td>265</td>
      <td>2</td>
      <td>131.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>131.80</td>
    </tr>
    <tr>
      <th>29</th>
      <td>94052446</td>
      <td>2</td>
      <td>11/06/2017 8:30:50 PM</td>
      <td>11/07/2017 12:00:00 AM</td>
      <td>1</td>
      <td>30.83</td>
      <td>1</td>
      <td>N</td>
      <td>132</td>
      <td>23</td>
      <td>1</td>
      <td>80.00</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>18.56</td>
      <td>11.52</td>
      <td>0.3</td>
      <td>111.38</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2440</th>
      <td>63574825</td>
      <td>1</td>
      <td>07/26/2017 10:26:58 PM</td>
      <td>07/26/2017 10:26:58 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>162</td>
      <td>264</td>
      <td>2</td>
      <td>5.50</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>6.80</td>
    </tr>
    <tr>
      <th>15916</th>
      <td>47368116</td>
      <td>1</td>
      <td>06/29/2017 7:30:30 PM</td>
      <td>06/29/2017 7:43:29 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>79</td>
      <td>148</td>
      <td>3</td>
      <td>8.50</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>10.30</td>
    </tr>
    <tr>
      <th>1350</th>
      <td>91619825</td>
      <td>2</td>
      <td>10/30/2017 8:20:29 AM</td>
      <td>10/30/2017 8:20:38 AM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>193</td>
      <td>193</td>
      <td>1</td>
      <td>2.50</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.66</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>3.96</td>
    </tr>
    <tr>
      <th>246</th>
      <td>78660848</td>
      <td>1</td>
      <td>09/18/2017 8:50:53 PM</td>
      <td>09/18/2017 8:51:03 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>145</td>
      <td>145</td>
      <td>2</td>
      <td>2.50</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>3.80</td>
    </tr>
    <tr>
      <th>17788</th>
      <td>58079289</td>
      <td>1</td>
      <td>07/08/2017 12:54:02 AM</td>
      <td>07/08/2017 12:55:03 AM</td>
      <td>2</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>158</td>
      <td>158</td>
      <td>3</td>
      <td>2.50</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>3.80</td>
    </tr>
  </tbody>
</table>
<p>22699 rows × 18 columns</p>
</div>




```python
sorted_amount = df['total_amount'].sort_values(ascending = False)
sorted_amount.head(20)
# Sort the data by total amount and print the top 20 values
```




    8476     1200.29
    20312     450.30
    13861     258.21
    12511     233.74
    15474     211.80
    6064      179.06
    16379     157.06
    3582      152.30
    11269     151.82
    9280      150.30
    1928      137.80
    10291     131.80
    6708      126.00
    11608     123.30
    908       121.56
    7281      120.96
    18130     119.31
    13621     115.94
    13359     111.95
    29        111.38
    Name: total_amount, dtype: float64




```python
sorted_amount.tail(20)
# Sort the data by total amount and print the bottom 20 values
```




    14283      0.31
    19067      0.30
    10506      0.00
    5722       0.00
    4402       0.00
    22566      0.00
    1646      -3.30
    18565     -3.80
    314       -3.80
    5758      -3.80
    5448      -4.30
    4423      -4.30
    10281     -4.30
    8204      -4.80
    20317     -4.80
    11204     -5.30
    14714     -5.30
    17602     -5.80
    20698     -5.80
    12944   -120.30
    Name: total_amount, dtype: float64




```python
df['payment_type'].value_counts()
# How many of each payment type are represented in the data?
```




    1    15265
    2     7267
    3      121
    4       46
    Name: payment_type, dtype: int64




```python
# Payment type 1 is credit card and 2 is cash
# What is the average tip for trips paid for with credit card?
mask = df['payment_type'] == 1
print(df[mask]['tip_amount'].mean())

# What is the average tip for trips paid for with cash?
mask1 = df['payment_type'] == 2
df[mask1].mean()['tip_amount']
```

    2.7298001965279934





    0.0




```python
df['VendorID'].value_counts()
# How many times is each vendor ID represented in the data?
```




    2    12626
    1    10073
    Name: VendorID, dtype: int64




```python
# df['VendorID'].value_counts('')
df.groupby(['VendorID']).mean(numeric_only = True)[['total_amount']]
# What is the mean total amount for each vendor?
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>total_amount</th>
    </tr>
    <tr>
      <th>VendorID</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>16.298119</td>
    </tr>
    <tr>
      <th>2</th>
      <td>16.320382</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Filter the data for credit card payments only
mask = df[df['payment_type'] == 1]
mask

# Filter the data for passenger count only
mask1 = df['payment_type'] == 2
df[mask1]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>30841670</td>
      <td>2</td>
      <td>04/15/2017 11:32:20 PM</td>
      <td>04/15/2017 11:49:03 PM</td>
      <td>1</td>
      <td>4.37</td>
      <td>1</td>
      <td>N</td>
      <td>4</td>
      <td>112</td>
      <td>2</td>
      <td>16.5</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>17.8</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8433159</td>
      <td>2</td>
      <td>02/04/2017 4:17:07 PM</td>
      <td>02/04/2017 4:29:14 PM</td>
      <td>1</td>
      <td>1.20</td>
      <td>1</td>
      <td>N</td>
      <td>234</td>
      <td>249</td>
      <td>2</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>9.8</td>
    </tr>
    <tr>
      <th>18</th>
      <td>35388828</td>
      <td>2</td>
      <td>04/10/2017 6:12:58 PM</td>
      <td>04/10/2017 6:17:39 PM</td>
      <td>2</td>
      <td>0.63</td>
      <td>1</td>
      <td>N</td>
      <td>263</td>
      <td>262</td>
      <td>2</td>
      <td>5.0</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>6.8</td>
    </tr>
    <tr>
      <th>20</th>
      <td>110690689</td>
      <td>1</td>
      <td>12/30/2017 11:52:44 PM</td>
      <td>12/30/2017 11:58:57 PM</td>
      <td>1</td>
      <td>1.10</td>
      <td>1</td>
      <td>N</td>
      <td>166</td>
      <td>238</td>
      <td>2</td>
      <td>6.5</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>7.8</td>
    </tr>
    <tr>
      <th>27</th>
      <td>99525452</td>
      <td>2</td>
      <td>11/24/2017 10:48:13 AM</td>
      <td>11/24/2017 10:52:57 AM</td>
      <td>1</td>
      <td>0.85</td>
      <td>1</td>
      <td>N</td>
      <td>237</td>
      <td>161</td>
      <td>2</td>
      <td>5.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>6.3</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>22673</th>
      <td>58511484</td>
      <td>1</td>
      <td>07/09/2017 5:25:16 PM</td>
      <td>07/09/2017 5:29:16 PM</td>
      <td>1</td>
      <td>0.80</td>
      <td>1</td>
      <td>N</td>
      <td>79</td>
      <td>4</td>
      <td>2</td>
      <td>5.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>5.8</td>
    </tr>
    <tr>
      <th>22675</th>
      <td>58407519</td>
      <td>1</td>
      <td>07/09/2017 9:09:10 AM</td>
      <td>07/09/2017 9:15:31 AM</td>
      <td>1</td>
      <td>1.70</td>
      <td>1</td>
      <td>N</td>
      <td>148</td>
      <td>137</td>
      <td>2</td>
      <td>7.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>8.3</td>
    </tr>
    <tr>
      <th>22688</th>
      <td>66450599</td>
      <td>2</td>
      <td>08/05/2017 9:23:29 PM</td>
      <td>08/05/2017 9:26:11 PM</td>
      <td>3</td>
      <td>0.44</td>
      <td>1</td>
      <td>N</td>
      <td>230</td>
      <td>163</td>
      <td>2</td>
      <td>4.0</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>5.3</td>
    </tr>
    <tr>
      <th>22694</th>
      <td>14873857</td>
      <td>2</td>
      <td>02/24/2017 5:37:23 PM</td>
      <td>02/24/2017 5:40:39 PM</td>
      <td>3</td>
      <td>0.61</td>
      <td>1</td>
      <td>N</td>
      <td>48</td>
      <td>186</td>
      <td>2</td>
      <td>4.0</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>5.8</td>
    </tr>
    <tr>
      <th>22696</th>
      <td>74239933</td>
      <td>2</td>
      <td>09/04/2017 2:54:14 PM</td>
      <td>09/04/2017 2:58:22 PM</td>
      <td>1</td>
      <td>0.42</td>
      <td>1</td>
      <td>N</td>
      <td>107</td>
      <td>234</td>
      <td>2</td>
      <td>4.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>5.3</td>
    </tr>
  </tbody>
</table>
<p>7267 rows × 18 columns</p>
</div>




```python
# Calculate the average tip amount for each passenger count (credit card payments only)

mask.groupby(['passenger_count']).mean(numeric_only = True)[['tip_amount']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tip_amount</th>
    </tr>
    <tr>
      <th>passenger_count</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2.610370</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.714681</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2.829949</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2.726800</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2.607753</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2.762645</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2.643326</td>
    </tr>
  </tbody>
</table>
</div>



<img src="images/Construct.png" width="100" height="100" align=left>

## PACE: **Construct**

**Note**: The Construct stage does not apply to this workflow. The PACE framework can be adapted to fit the specific requirements of any project. 




<img src="images/Execute.png" width="100" height="100" align=left>

## PACE: **Execute**

Consider the questions in your PACE Strategy Document and those below to craft your response.


### **Given your efforts, what can you summarize for DeShawn and the data team?**

*Note for Learners: Your notebook should contain data that can address Luana's requests. Which two variables are most helpful for building a predictive model for the client: NYC TLC?*

    After examining the data, I think the two variables that are likely to be the most helpful while building a predictive model are total_Amount and the trip_distance.

**Congratulations!** You've completed this lab. However, you may not notice a green check mark next to this item on Coursera's platform. Please continue your progress regardless of the check mark. Just click on the "save" icon at the top of this notebook to ensure your work has been logged.
