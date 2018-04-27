# -*- coding: utf-8 -*-
"""
Created on Thu Apr 26 22:17:37 2018

@author: Sudhiram
"""

# Cheatsheet to run errand

### Open a file in Read mode and extract the contents into an array 
```python
with open(file_name) as f:
  arrVar = f.read().splitlines()
```

### Split a string into array 
```python
arrVar = strVar.split("DELIMITTER")
```

### Join an array into string 
```python
strVar = str.join("", arrVar)
```

### Iterate two lists at the same time 
```python
list1 = [1, 2, 3]
list2 = [4 ,5, 6]
  for (x,y) in zip(list1, list2):
    print (x,y)
```

### Find unique elements in list 
```python 
listVar = ["cat", "dog", "cat"]
np.unique(listVar)
```

### Remove dupicate elements between two lists
```python 
a = ["abc", "def", "ijk", "lmn", "opq", "rst", "xyz"]
b = ["ijk", "lmn", "opq", "rst", "123", "456", ]
[elem for elem in b if elem not in a ]
(or)
list(set(b)-set(a))
```
### Convert String to Datetime 
```python 
from datetime import datetime
dt_obj = datetime.strptime('Jun 1 2005  1:33PM', '%b %d %Y %I:%M%p')
dt_obj.day 
dt_obj.month 
dt_obj.year
dt_obj.hour
dt_obj.minute
dt_obj.second
```

### Convert Datetime to String 
```python 
dt_obj.strftime('%d-%m-%Y')
```

### Sort data based on Date
```python 
import operator
l = [{'date': '2010-04-01','people': 1047, 'hits': 4522},{'date': '2010-04-03', 'people': 617, 'hits': 2582},{'date': '2010-04-02', 'people': 736, 'hits': 3277}]
sorted( l, key = operator.itemgetter('date') )
```

### Misc printing stuff
```python
"Hello {0}".format("World")

l = [1, 2, 3]
len(l) => 3 

range(1,3) => [1, 2]
``` 


### Getoptions
```python 
import sys, getopt
    try:
        opts, args = getopt.getopt(sys.argv[1:], "h:ifile",  ["ifile=", "h=", "step=", "debug"])
    except getopt.GetoptError as err:
        print str(err)
        usage()
```


## Pattern Matching 
### Extract patterns from string 
```python
pattern = re.search('\s*(\S+)\s*:', strVar, [re.IGNORECASE]) 
strVar2 = pattern.group(1)
```

### Search and replace a pattern in string 
```python
newStr = re.sub('S', 'X', strVar)
```
