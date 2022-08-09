## T1614.001-1 - Discovery System Language by Registry Query
|||
|-|-|
|**Test ID**|T1614.001-1|
|**Testable Client Platforms**|Windows Server 2003, 2008, 2008 R2, 2012<br>Windows XP, Vista, 7, 8, 10, 11|
|**Required Tools**|[S0075 "REG" (Native to Windows)](https://attack.mitre.org/software/S0075/)|
|**Target**|Client|
|**Last Updated**|2022-08-09|

Using the reg query, we can retrieve language information from registry about the client system, which assists in discovering the location of a system.

### Test Procedure
|Prerequisites|
|-|
|The client is logged in as a regular user.|

|#|Instruction|
|-|-|
|1|Open command prompt as a regular user.|
|2|Enter the command “reg query HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Language” and hit enter.|
|3|If the terminal prints out a list of information detailing the install langauge region and ID and the InstallLanguageFallback ID's, the test has been completed successfully.|

<!-- TODO ADD IMAGE -->

### Network Traffic
During testing, no network traffic was identified which could be attributed to the test.

### Resources
Microsoft Documentation for the reg query command: https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc742028(v=ws.11) 