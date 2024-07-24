# Simplifyd WAN Edge firmware updater

## Steps to update the firmware on the Simplifyd WAN Edge device
1) Download the following files from here
   - `boot.fat`
   - `mbr.img`
   - `root.squashfs`
   - `updater` - the version to download depends on your operating system. If you are on a Windows machine, download the `updater.exe`. If you are on an intel MacOS machine, download the `updater` file instead. We currently do not have a version of this file for Apple based silicon MacOS machines. If you happen to be using one of these currently unsupported machines, please send us an email and we would make a compatible version available to you.
2) Connect the power adapter to the device and power it on.
3) Connect your computer via an ethernet cable to the `lan0` port of the device. Take a look at the image below to help you determine what the port names are. The default IP address for the `lan0` port is `192.168.200.1/24`
4) After the files are downloaded to a directory perform the following steps depending on your operating system:

### Command to update device
After the updater executable and firmware images have been downloaded into a directory, run the following commands from the same directory.
Note that the default LAN IP of the 
#### MacOS & Unix
```
chmod +x updater
./updater <IP Address of lan0>

example:
./updater 192.168.200.1
```

#### Windows
```
./updater.exe <IP Address of lan0>

example:
./updater.exe 192.168.200.1
```
