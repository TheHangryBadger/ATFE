## T1614.001-2 - Discovery System Language with CHCP
|||
|-|-|
|**Test ID**|T1614.001-2|
|**Testable Client Platforms**|Windows Server 2008, 2008 R2, 2012<br>Windows Vista, 7, 8, 10, 11|
|**Required Tools**|["CHCP" (Native to Windows)](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc733037(v=ws.11))|
|**Target**|Client|
|**Last Updated**|2022-08-09|

Using the CHCP command we can get a numerical ID which can be looked up to identify the language of the system.

### Test Procedure
|Prerequisites|
|-|
|The client is logged in as a regular user.|

|#|Instruction|
|-|-|
|1|Open command prompt as a regular user.|
|2|Enter the command “chcp” and hit enter.|
|3|Take the ID and match it with microsofts Code Page Identifiers list found here: https://docs.microsoft.com/en-us/windows/win32/intl/code-page-identifiers|
|4|If the identified information matches the client system, the test has been completed successfully.|

<!-- TODO ADD IMAGE -->

### Network Traffic
During testing, no network traffic was identified which could be attributed to the test.

### Resources
Microsoft Documentation for the chcp command: https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc733037(v=ws.11) 
Microsoft Code Page Identifiers table: https://docs.microsoft.com/en-us/windows/win32/intl/code-page-identifiers 