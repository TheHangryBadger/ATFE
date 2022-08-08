# Attack Paths: Quantum Ransomware
|||
|-|-|
|**Type**|Ransomware Attack|
|**Last Updated**|2022-08-08|

This attack path shows the various attack methods used in an attack with the quantum ransomware, as described by thedfirreport in this article from April 2022: https://thedfirreport.com/2022/04/25/quantum-ransomware/ 

##  The Attack
Initial access was achieved using IcedID which is believed to have compromised a workstation through an ISO image sent via email (unconfirmed). 

The workstation compromised by IcedID then performed discovery using the following windows utilities native to windows: ipconfig, systeminfo, nltest, net and chcp. Additionally, it performed persistence using scheduled tasks on the beachhead. 

Later, Cobalt Strike was deployed using process hollowing and injection. AdFind was then run using a batch script to perform AD discovery, and network discovery using another batch script running nslookup to perform host discovery. 

Afterwards, Cobalt Strike dumped the LSASS memory and confirmed cracked credentials using WMI to perform remote WMI discovery tasks on a server. This server was then RDP’d into using the cracked credentials, and the attacker attempted but failed to load the Cobalt Strike DLL on said server. Following this CMD was used to execute a Cobalt Strike Beacon on said server which then connected to the beachhead as C&C. 

The threat actor then RDP’d to several servers on the network over the span of an hour, and then distributed the ransomware using the C$ share folder. This ransomware was then executed on each host using WMI and PsExec. 

A note was found indicating data exfiltration, but no evidence of this alleged exfiltration was found. 

## Relevant ID's
||||
|-|-|-|
|S0029|PS Exec|Sysinternals|
|S0039|NET|Native to Windows|
|S0100|IPConfig|Native to Windows|
|S0154|Cobalt Strike|Licensed Software/Malware|
|S0359|NLTEST|Native to Windows|
|S0483|IcedID||
|S0552|AdFind|Joeware.net|
||Query|Native to Windows|

|Tactics ID|Tactic Description|Matching Tests|
|-|-|-|
|T1003.001|OS Credential Dumping: LSASS Memory||
|T1018|Remote System Discovery|[T1018-1](../../Atomics/T1018 - Remote System Discovery#t1018-1-remote-system-discovery-using-net-view), [T1018-2](../../Atomics/T1018 - Remote System Discovery#t1018-2-remote-system-discovery-using-net-group)|