## 配置
+ OS: macOS 11.5.2 20F71 x86_64 / (SMBIOS: iMac19,1)
+ OpenCore: 0.7
+ CPU: Intel i3-9100
+ GPU: Intel UHD Graphics 630
+ Wi-Fi: BCM94360CS2 

## 存在问题
Hdmi显示屏紫屏；解决方法 注入花屏补丁

  #https://github.com/xzhih/one-key-hidpi/blob/master/README-zh.md
  bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"


## BIOS
Load UEFI Defaults

+ Advanced > Chipset Configuration  > Onboard HD Audio & Onboard HDMI HD Audio: Enabled
+ Advanced > Chipset Configuration  > VT-d: Disabled
+ Advanced > USB Configuration > XHCI Hand-off: Enabled
+ Advanced > CPU Configuration  > C States Support: Disabled
+ Advanced > Super IO Configuration > Serial Port: Disabled
+ Security > Secure Boot: Disabled
+ BOOT > CSM: Enabled



## macOS Tips

```
sudo pmset -c sleep 30
sudo pmset -c displaysleep 30
sudo pmset -c disksleep 30
sudo pmset -c hibernatemode 0
sudo pmset -c standby 0
sudo pmset -c autopoweroff 0
sudo pmset -c tcpkeepalive 1

# disable the Spotlight indexes
sudo mdutil -a -i off

# change host name
sudo scutil --set HostName mini
sudo scutil --set ComputerName mini
sudo scutil --set LocalHostName mini

sudo spctl --master-disable
```

- [acidanthera](https://github.com/acidanthera)
- [xjn819 blog](https://blog.xjn819.com/)
