# ADB commands

### Normal path in windows for SDK exec

```C:\Users\Username\AppData\Local\Android\Sdk\platform-tools>```

### Samsusng Galaxi activate debug mode 

```*#0808#```

### Commands
```adb start-server```

```adb kill-server```

#### List of devices
```adb devices```

#### Install Aplications from local apk
```adb install path_to_apk```

#### Copy files from device to local
```adb pull remote local```

#### Copy files from local to device
```adb push local remote```

#### Interactive Shell 
```adb shell```

Shell commands:

- Extract system data on screen

```dumpsys```

- System status

```dumpstate```

#### List Install Aplications
```adb shell pm list packages```

#### Obtain path from install app
```adb shell pm path com.ejemplo.app```

#### Download app.apk to local
```adb pull path/ejemplo/ap.apk```

#### Debug install aplication
```adb -d logcat [com.package.example]:I *:S```

```adb -d logcat [com.package.example] | find "keewords"```

#### Execute command to specific device
```adb -s deviceName command_to_run```

## Configure Local ADB trow Remote ADB ##
- Necesari same version of adb in Client and Server
- Server: ```adb -a -P 5037 nodaemon server```
- Client: ```adb -H [remoteIP] -P 5037 devices```
