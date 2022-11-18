# 📚 Case Study - Online Hotel Web Search: A. Data Exploration and Cleansing

<p align="right"> Using Python - Google Colab vs Power BI </p>

#

## IMPORT Library
```python

#import lib
#import thư viện
import pandas as pd
import numpy as np
import matplotlib as plt
import matplotlib.pyplot as plt
import seaborn as sns
from matplotlib import dates
import datetime
print('Completed import lib')

```
## IMPORT DATASET 

**1.Import csv file and check info**

```python
df =  pd.read_csv('/content/marketplace_data_2019.csv')
df.info()
```

![image](https://user-images.githubusercontent.com/101379141/201808490-8401cd03-c550-499b-a1f7-8b0e3c47e694.png)


**2.Checking Null Values**

```python
#Checking null Values
df.isnull().sum()
 ```

![image](https://user-images.githubusercontent.com/101379141/201808617-491cf006-3a10-4d64-bff1-4a303de2ab8f.png)

---> There is no Null Values

**3. Unpivot Dataframe**

```python
#Unpivot dataframe 
df_unpivot = pd.wide_to_long(df,
                             stubnames =['clicks', 'cost','bookings','booking_rev'],  #select columns
                             i = ['date','ttt_group'], #
                             j = 'Advertiser', 
                             sep ='_', 
                             suffix ='\w+')
print(df_unpivot.head())
```


![image](https://user-images.githubusercontent.com/101379141/201808854-9f569359-c84b-4f9d-a2bc-7693a0a7ce13.png)


**4. Transforming MultiIndex to Column"**


```python
#Transforming MultiIndex to Columns
df = df_unpivot.reset_index()
print(df.head())
df.info()
```

![image](https://user-images.githubusercontent.com/101379141/201809059-a51c70c9-f7a7-49cd-aeb9-3ba917c0a24a.png)


**5. Save file "**

```python
#Save file 
df.to_csv('Final_mindx.csv')
```

## IMPORT CLEAN FILE TO POWER BI

**1. Transform Data** 

Use First rows as Header, Change type of click,cost,bookings,booking_rev,month column to Number type. Remove First Column (order column)
- Source data :
![image](https://user-images.githubusercontent.com/101379141/201811749-42448661-d040-4aa3-b988-61f760e30967.png)

- Promoted header, Change type & Replace value :
![image](https://user-images.githubusercontent.com/101379141/201811790-dafc5346-5765-4d8e-ba52-a66bdb2f4266.png)

- Change data type and remove the first column (order column)  
![image](https://user-images.githubusercontent.com/101379141/201811834-218fad64-ac8d-4e04-bc63-ecea2f3f13f7.png)

**2.Add new measure dax - Conversion rate, % Booking, Cost/Booking, Profit/Cost, Rev_Per_booking**

- Conversion rate : calculated by dividing the number of bookings by the number of clicks
![image](https://user-images.githubusercontent.com/101379141/201810659-6781dbb1-b196-46a6-ad27-fd372ea12c21.png)

- % Booking : Calculate the percent of booking monthly 
![image](https://user-images.githubusercontent.com/101379141/201811251-3b597fca-9431-4b3d-84cc-bf0ca65fd4ce.png)

- Cost/Booking: The Average Cost per booking 
![image](https://user-images.githubusercontent.com/101379141/201811367-eb7d2578-603c-42bf-80d7-6d82fe5a56e9.png)

- Profit/Cost : The profit make from cost
![image](https://user-images.githubusercontent.com/101379141/201811526-4572e993-434b-4b1d-b536-6f1e40963b24.png)

- Rev_Per_booking : The Revenue per booking
![image](https://user-images.githubusercontent.com/101379141/201811606-cd77eda4-7817-46cc-b4d6-49c7d337c4f0.png)



