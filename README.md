# AutoBuildImmortalWrt
[![GitHub](https://img.shields.io/github/license/wukongdaily/AutoBuildImmortalWrt.svg?label=LICENSE&logo=github&logoColor=%20)](https://github.com/wukongdaily/AutoBuildImmortalWrt/blob/master/LICENSE)

# 🤔 这是什么？
这是一个工作流。可以快速构建带docker且支持自定义固件大小的 immortalWrt
> - 支持自定义固件大小，默认1GB 
> - 支持预安装docker（可选）
> - 支持 x86-64 和 rockchip 两个平台（后续会增加）
> - 新增用户预设置 pppoe 拨号功能


## 该固件默认属性？（必读）
- 该固件刷入【单网口设备】默认采用DHCP模式，自动获取ip地址，类似NAS的做法。
- 该固件刷入【多网口设备】默认wan口采用DHCP模式，lan口ip地址为 `192.168.100.1` 。
- 若用户在工作流中勾选了 PPPoE 拨号信息，则WAN口改为 PPPoE 拨号模式。
- 上述特点，你都可以通过 `99-custom.sh` 配置和调整。

## 正常路由模式必读
- 一般wan口用于拨号或者自动获取ip地址，而其余lan口用于dhcp服务给其他设备分配ip地址。
- 这种情况下，你可以修改路由器的默认ip地址 `192.168.100.1` 比如你可以修改为 `192.168.80.1 ` 诸如此类。
- 没错，修改此ip地址无非就是为了避免跟光猫或者跟家庭中的其他路由器网段冲突，大多数用户保持默认即可。

## 旁路由的用户必读
- 近期不少用户修改配置文件中的默认ip地址，误认为这个工作流可以直接设置旁路ip地址。<br>这是巨大的误解，这样设置就乱套了。
- 旁路的逻辑应该是单网口模式。根据上述的固件属性可知：单网口默认采取`dhcp模式`。
- 用户应当自行在上一级路由器查看给imm路由器分配的ip地址，然后通过该ip来访问imm后台页面，<br>在imm后台页面中，根据自己主路由的网段，自行配置旁路的ip地址。


## 🌟鸣谢
### https://github.com/immortalwrt
