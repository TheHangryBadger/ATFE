## T1082-1 System Information Discovery using SYSTEMINFO
|||
|-|-|
|**Test ID**|T1082-1|
|**Testable Client Platforms**|Windows Server 2003, 2008, 2008 R2, 2012, 2016<br>Windows XP, Vista, 7, 8|
|**Required Tools**|S0096 "SYSTEMINFO" (native to windows)|
|**Target**|Client|
|**Last Updated**|2022-08-08|

Using the native systeminfo command we discover information about the local system.

### Test Procedure
|Prerequisites|
|-|
|The client must be logged in as a regular user.|

|#|Instruction|
|-|-|
|1|Open command prompt as a regular user.|
|2|Enter the command "systeminfo", hit enter, and wait for the results.|
|3|If the terminal prints out a list of domains, computers and or resources shared by the client, the test has been completed successfully.|

<!--TODO: ADD IMAGE     <img src="T1018-1.png" height="160px"> -->
### Network Traffic
During initial testing, network traffic was not immediately determinable from packet captures.

### Resources
Microsoft Documentation for the systeminfo command: 
https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc771190(v=ws.11) 