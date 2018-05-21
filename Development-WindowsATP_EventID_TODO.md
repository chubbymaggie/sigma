# Windows Defender ATP backend implementation

The Windows Defender ATP backend requires a mapping between log sources/event
identifiers and ATP tables and event types contained there. The mapping is
mainly implemented in `WindowsDefenderATPBackend.generateMapItemNode()`.

## Sigma Windows Event IDs

Windows log sources and event identifiers that are contained in the rule
repository but not yet implemented in WDATP backend. Syntax of each item is:

* sigma-product sigma-service EventID

* windows application 1000
* windows application 1001
* windows application 524
* windows dns-server 150
* windows dns-server 770
* windows driver-framework 2003
* windows driver-framework 2100
* windows driver-framework 2102
* windows null 7045
* windows null 7036
* windows null 1
* windows powershell 4103
* windows powershell 4104
* windows powershell-classic 400
* windows security 517
* windows security 528
* windows security 529
* windows security 675
* windows security 1102
* windows security 4624
* windows security 4625
* windows security 4776
* windows security 4656
* windows security 4657
* windows security 4658
* windows security 4660
* windows security 4661
* windows security 4663
* windows security 4698
* windows security 4707
* windows security 4719
* windows security 4732
* windows security 4738
* windows security 4765
* windows security 4766
* windows security 4768
* windows security 4769
* windows security 4771
* windows security 4776
* windows security 4769
* windows security 4794
* windows security 5136
* windows security 5140
* windows security 5145
* windows system 16
* windows system 104
* windows system 1031
* windows system 1032
* windows system 1033
* windows system 1034
* windows system 4697
* windows system 7045
* windows taskscheduler 106
* windows wmi 5859
* windows wmi 5861

## WDATP MiscEvent ActionTypes

Clarification required:
* windows sysmon 10: MiscEvents ActionType OpenProcess or SetThreadContextRemote? Field GrantedAccess missing.

No appropriate data source found in ATP:
* windows sysmon 6 (Driver Loaded)
* windows sysmon 17 (Pipe Creation)
* windows sysmon 18 (Pipe Connected)
