---
title: "Data in the World of Warcraft Auction House"
permalink: /WoW/
header:
  overlay_image: "/images/warcraft.png"
---
# WoW AH Analysis
[View on GitHub](https://github.com/midumass/DSC-530/tree/master/10.4) 

### Purpose
Analyzing data pulled from the World of Warcraft Auction House

### Technologies
* Python

### Data
[Sampled Dataset](https://github.com/midumass/DSC-530/blob/master/10.4/ah_item_small.csv) 

### Results
![Sample Image](images/DSC-530/AHpricedist.png)
```py
bid = df['bid']
print('Mean =', bid.mean(),
      '\nMedian =', bid.median(), 
      '\nSD =', bid.std(), 
      '\nVariance =', bid.var())

Mean = 154722561.31587 
Median = 6004355.0 
SD = 2389442273.198373 
Variance = 5.709434376947407e+18
```
![Sample Image](images/DSC-530/AHqualdist.png)
```py
qual = df['quality'].value_counts()
print(qual)

1.0    36333
2.0    33956
3.0    20010
4.0     9494
0.0      185
5.0       22
```

![Sample Image](images/DSC-530/AHlevdist.png)
```py
reqLvl = df['requiredLevel'].value_counts()
reqLvl.head(5)

0.0      48241
120.0     6560
1.0       4829
100.0     4155
110.0     2437
```