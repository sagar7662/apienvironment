
1. Add configuration in your project like this:

  ![alt text](https://raw.githubusercontent.com/sagar7662/apienvironment/master/Images/addConfiguration.png)

2. We need to create new user-defined setting(API_BASEURL) in Xcode target build setting like this:

  ![alt text](https://raw.githubusercontent.com/sagar7662/apienvironment/master/Images/userDefinedSetting.png)

3. Map above new user-defined setting with `info.plist` file to get environment.

  ``` javascript
  Key                 Value

  APIBaseUrl          $(API_BASEURL)
  ```   

  ![alt text](https://raw.githubusercontent.com/sagar7662/apienvironment/master/Images/addKeyValueInPlist.png)

4. Add schemes for different configurations.

  ![alt text](https://raw.githubusercontent.com/sagar7662/apienvironment/master/Images/addNewScheme.png)
  
5. Do some code in `AppDelegate.swift` to get selected scheme environment.

 ```
if let bundleInfo = Bundle.main.infoDictionary, let url = bundleInfo["APIBaseUrl"] as? String {
            print(url)
    }
  ```

6. Now, edit your scheme for different build configuration.

  ![alt text](https://raw.githubusercontent.com/sagar7662/apienvironment/master/Images/buildConfInNewScheme.png)
