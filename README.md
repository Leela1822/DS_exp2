# DS_exp2
# DataScience_exp2
# AIM:
To read a given dataset and remove outliers and save a new dataframe.

# ALGORITHM:
(1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them

# PROGRAM:
```
import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

df = pd.read_csv("/content/heights.csv")

sns.boxplot(data=df)

sns.scatterplot(data=df)

max =df['height'].quantile(0.90)

min =df['height'].quantile(0.15)

max

min

dq = df[((df['height']>=min)&(df['height']<=max))]

dq

low = min-1.5*iqr

high = max+1.5*iqr

dq = df[((df['height']>=min)&(df['height']<=max))]

dq
```

# ZSCORE:
```
import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}

df = pd.DataFrame(data)

df

sns.boxplot(data=df)

z = np.abs(stats.zscore(df))

print(df[z['weight']>3])

val = [12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]

out=[]

def d_o(val):

ts=3

m=np.mean(val)

sd=np.std(val)

for i in val:

z=(i-m)/sd

if np.abs(z)>ts:

  out.append(i)
return out

op = d_o(val)

op
```
# OUTPUT:
![image](https://github.com/Leela1822/DS_exp2/assets/106167639/fb7257f9-aa9f-4728-bcf6-798af592b6c4)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/36d8b6ee-f0e1-44bf-aa83-cfe176f9bfb5)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/62ece1d2-77f8-4e39-82ad-58deaf8b5787)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/1acd3bf2-3b34-49bc-bf51-20abf0b76101)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/88466cd5-2cf3-41e4-b48d-dd53884b4846)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/aceb579e-8fbe-4418-9508-88d55682dc89)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/a74178df-af2d-447b-baab-14ef5f4b8ef0)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/13092026-df0d-4476-8f63-e51c78d8c670)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/4bd40d33-4108-4be1-84f9-c4a7f92a3810)


![image](https://github.com/Leela1822/DS_exp2/assets/106167639/43090faa-56ee-4d18-be50-8fc554f365cf)



# RESULT:
Thus, the given data is read,remove outliers and save a new dataframe was created and executed successfully.
