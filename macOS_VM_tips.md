[Source](https://www.intoguide.com/install-macos-catalina-virtualbox-windows-pc/)
## _If having trouble finding 64bit in the dropdown versions menu, ensure that HyperV is disabled and that you have Virtualization enabled in your BIOs_

# Before starting the new VM
Execute the following commands (replace `macOS 10.15` with whatever you named your VM)

``` bash
cd "C:\Program Files\Oracle\VirtualBox\" 
VBoxManage.exe modifyvm "macOS 10.15" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff 
VBoxManage setextradata "macOS 10.15" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac11,3" 
VBoxManage setextradata "macOS 10.15" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0" 
VBoxManage setextradata "macOS 10.15" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple" 
VBoxManage setextradata "macOS 10.15" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc" 
VBoxManage setextradata "macOS 10.15" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1
```
# For AMD Users
``` bash
cd "C:\Program Files\Oracle\VirtualBox\"
```

``` bash
VBoxManage.exe modifyvm "Mac" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff
```

``` bash
VBoxManage setextradata "Mac" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac11,3"
```

``` bash
VBoxManage setextradata "Mac" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0"
```

``` bash
VBoxManage setextradata "Mac" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple"
```

``` bash
VBoxManage setextradata "Mac" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"
```

``` bash
VBoxManage setextradata "Mac" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 1
```

``` bash
VBoxManage modifyvm "Mac" --cpu-profile "Intel Core i7-6700K"
```

``` bash
VBoxManage setextradata "Mac" VBoxInternal2/EfiGraphicsResolution 1920x1080
```
