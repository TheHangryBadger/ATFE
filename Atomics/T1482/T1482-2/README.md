## T1482-2 Windows - Discover domain trusts with nltest
|||
|-|-|
|**Test ID**|T1482-2|
|**Testable Client Platforms**|Windows Server 2003 SP1, 2003 R2, 2008, 2008 R2, 2012<br>Windows 8, 10, 11|
|**Required Tools**|[S0359](https://attack.mitre.org/software/S0359/) ["NLTEST" (native to windows or downloadable via RSAT)](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc731935(v=ws.11))|
|**Target**|Client|
|**Last Updated**|2022-08-10|

Using the native nltest command we can obtain information about the domain, such as a list of domain controllers and query trusts of the domain.

### Test Procedure
|Prerequisites|
|-|
|The client must be logged in as a regular Domain user.|
|The client must be Domain joined.|
|The client must have [Remote Server Administration Tools (RSAT)](https://www.microsoft.com/en-us/download/details.aspx?id=45520) installed.|

|#|Instruction|Expected Outcome|Image|
|-|-|-|-|
|1|Open command prompt as a regular user.|||
|2|Enter the command "nltest /domnain_trusts", hit enter, and wait for the results.|A list of domain trusts is printed in command prompt.|![](T1482-2.2.png)|
|3|If the terminal prints out a list of domain trusts, the test is completed successfully.|||

![](T1482-2.2.png)

### Network Traffic
During initial testing, network traffic was not immediately determinable from packet captures.

### Resources
[Microsoft Documentation for the nltest command](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc731935(v=ws.11))<br>
[Microsoft Download Page for Remote Server Administration Tools (RSAT)](https://www.microsoft.com/en-us/download/details.aspx?id=45520)