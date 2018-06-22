# This Tutorial will show you the steps to follow to interface C++ code with Python 

## Step 1:
You need to create an interface point in C++ code where the Python can interface with C++ code. 
Lets say we need to use LicenseModel class in Python code then you need to do the following 

#### Original Code:
```
class Shape () {

}
```

#### New Code:
```
class Shape () {

}

extern "C" {
	Shape* Shape_new(const char* name) {  return new Shape(name); }
	bool ShapeValid_new(Shape* shapeObj) { return shapeObj->valid(); }
}
```
