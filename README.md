# 日常脚本小技巧

Daily shell script~

## VirtualBox

- 后台启动

```cmd
@echo off
pushd "C:\Program Files\Oracle\VirtualBox"

VBoxManage.exe startvm "HadoopMaster" -type headless
VBoxManage.exe startvm "HadoopSlave1" -type headless
```

- 停止虚拟机

```cmd
@echo off
pushd "C:\Program Files\Oracle\VirtualBox"

VBoxManage.exe controlvm "HadoopMaster" poweroff 
VBoxManage.exe controlvm "HadoopSlave1" poweroff 
```
