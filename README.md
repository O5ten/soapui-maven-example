# SoapUI Maven Automation Example

This is an example setup for SoapUI-maven integration using a plain very basic pom to power up the soapui maven plugin.
It can be used to bring API test-automation to your project or to use it as a service-monitoring tool. 

Run with:
```bash
   mvn clean install
```

The SoapUI project contains one testsuite and a mockService on 8088 with a single resource /hello

The only testcase has three steps.
### 1. Start the mockservice
```
  http://localhost:8088/hello
```
which returns 
```json
{
   "hello": "world"
}
```

### 2. HTTP GET Request to http://localhost:8088/hello
And one assertion
```
Assert that payload contains "world"
```

### 3. Stop the mockservice