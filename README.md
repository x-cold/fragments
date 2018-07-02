# 日常脚本小技巧

Daily shell script~

## 进程控制

## Kill Process

```bash
sudo kill -s 9 $(ps aux | grep 'node' | grep -v grep|  awk '{print $2}')
```

```bash
sudo kill `pgrep vim`
```

## Fork Bomb

> Detail: https://linux.cn/article-5685-1.html

```bash
:(){:|:&};:
```

## VirtualBox

- windows 后台启动

```cmd
@echo off
pushd "C:\Program Files\Oracle\VirtualBox"

VBoxManage.exe startvm "HadoopMaster" -type headless
VBoxManage.exe startvm "HadoopSlave1" -type headless
```

- windows 停止虚拟机

```cmd
@echo off
pushd "C:\Program Files\Oracle\VirtualBox"

VBoxManage.exe controlvm "HadoopMaster" poweroff 
VBoxManage.exe controlvm "HadoopSlave1" poweroff 
```
