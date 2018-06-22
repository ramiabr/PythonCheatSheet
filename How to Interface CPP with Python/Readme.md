# This Tutorial will show you the steps to follow to interface C++ code with Python 

## Step 1:
You need to create an interface point in C++ code where the Python can interface with C++ code. 
Lets say we need to use LicenseModel class in Python code then you need to do the following 

#### Original Code:
```
class LicenseModel () {

}
```

#### New Code:
```
class LicenseModel () {

}

extern "C" {
	LicenseModel* LicenseModel_new(const char* licenseKey) {  return new LicenseModel(licenseKey); }
	bool isLicenseKeyValid_new(LicenseModel* lic_model) { return lic_model->isLicenseKeyValid(); }
}
```
