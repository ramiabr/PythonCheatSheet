### Cheatsheet to run errand

# Open a file in Read mode and extract the contents into an array 
```python
with open(file_name) as f:
  arrVar = f.read().splitlines()
```

# Split a string into array 
arrVar = strVar.split("DELIMITTER")

# Join an array into string 
strVar = str.join("", arrVar)

## Pattern Matching 
# Extract patterns from string 
pattern = re.search('\s*(\S+)\s*:', strVar, [re.IGNORECASE]) 
strVar2 = pattern.group(1)

# Search and replace a pattern in string 
newStr = re.sub('S', 'X', strVar)

