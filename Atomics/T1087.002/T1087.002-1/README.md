## T1087.002-1 Enumerate all accounts (Domain)
|||
|-|-|
|**Test ID**|T1087.002-1|
|**Testable Client Platforms**|Windows Server 2000, 2003, 2008, 2008 R2, 2012, 2016<br>Windows XP, Vista, 7, 8, 10, 11|
|**Required Tools**|[S0039](https://attack.mitre.org/software/S0039/) ["NET" (native to windows)](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc754051(v=ws.11))|
|**Target**|Client|
|**Last Updated**|2022-08-10|

Using the native NET command we can obtain information about the domain, more specifically the users and groups in it.

### Test Procedure
|Prerequisites|
|-|
|The client must be logged in as a regular Domain user.|
|The client must be Domain joined.|

|#|Instruction|Expected Outcome|Image|
|-|-|-|-|
|1|Open command prompt as a regular user.|||
|2|Enter the command "net user /domain", hit enter, and wait for the results.|A list or matrix of domain users is printed in the command prompt.||
|3|Enter the command "net group /domain", hit enter, and wait for the results.|A list of domain groups is printed in the command prompt.||
|4|If the terminal prints out a list of domain trusts, the test is completed successfully.|||



### Network Traffic
*Pending Testing*

### Resources
[Microsoft Documentation for the NET GROUP command](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc754051(v=ws.11))<br>
[Microsoft Documentation for the NET USER command](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc771865(v=ws.11))