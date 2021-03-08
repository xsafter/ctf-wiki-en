# Android key code positioning


AndroidManifest.xml file


- package name
Apk main activity, hidden program without main activity


Application is the earliest in the java layer,


## Sequence Analysis


The most common and useful method is that we follow the logic of the program to view the code of the program for analysis, but when the program code is particularly large, the efficiency of this method is relatively low, and other methods are needed to assist.


## String positioning method


The so-called string positioning method is to locate the corresponding function by the string that appears during the running of the program. Strings may be hard-coded directly into the program, or they may be indexed by the string id. This method is convenient to use, but now, it is possible that the string will be separated or first encrypted and decrypted dynamically during the running process.


Strings we might be interested in may have


- Program error message
- Service
- Broadcast


## Sensitive API positioning


The so-called sensitive API positioning method means that we determine which functions the program may call based on the execution behavior of the program. This method requires us to be familiar with the API in Android. In general, we may focus on the following aspects


- Control event function
    - onclick

    - show

    - Toast

- Network function
    - HttpGet

    - HttpPost

    - HttpUriRequest

    - socket

- send messages
- Call
- Positioning
- and many more




## log信息


The so-called log information is the string information output by the Android program at runtime. This part of the information will not be reflected in our interface. Therefore, we need to use other auxiliary tools to analyze. For example, we can use ddms to assist the analysis. For log information, we can consider two aspects


- Use the log information generated by the program itself
- Decompile the code yourself, insert the log information, and repackage it for analysis.


## Stack Tracking


We can use the method provided by ddms to call the chain information to determine the current calling relationship of the program.


## hook


- xposed

- cydia



## monitor



- Run log, generated by the program, generated by the system
- Thread tracing
- Method call chain


## Dynamic debugging