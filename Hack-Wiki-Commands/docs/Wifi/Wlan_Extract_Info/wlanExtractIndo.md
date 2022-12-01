# Windows Wifi Info

Extract the list of all WLAN save on the host. Run the command on cmd or powershell terminal

```netsh.exe wlan show profiles```

Select some of profile of the list and replace for the name on the comand

```netsh.exe wlan show profiles name='some profile WLAN name' key=clear```
