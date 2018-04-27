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
