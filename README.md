# AutoBuildImmortalWrt
[![GitHub](https://img.shields.io/github/license/wukongdaily/AutoBuildImmortalWrt.svg?label=LICENSE&logo=github&logoColor=%20)](https://github.com/PrestonHee/AutoBuildImmortalWrt/blob/master/LICENSE)

# 🤔 这是什么？
这是一个工作流。可以快速构建带docker且支持自定义固件大小的 immortalWrt
> - 支持自定义固件大小，默认1GB 
> - 支持预安装 docker（可选）
> - 支持 x86_64 和 rockchip 两个平台（后续会增加）
> - 新增用户预设置 pppoe 拨号功能


## 该固件默认属性？（必读）
- 【单网口设备】默认采用DHCP模式，自动获取ip地址。
- 【多网口设备】默认wan口采用DHCP模式，lan口ip地址为 `192.168.100.1`。
- 若用户在工作流中勾选了 PPPoE 拨号信息，则wan口改为 PPPoE 拨号模式。
- 上述特点，你都可以通过 `/files/etc/uci-defaults/99-custom.sh` 配置和调整。

## 正常路由模式必读
- 一般wan口用于拨号或者自动获取ip地址，其余lan口用于dhcp服务分配ip地址。
- 你可以修改路由器的默认ip地址 `192.168.100.1` 例如修改为 `192.168.80.1` 等。
- 修改此ip地址就是为了避免跟光猫或其他路由器网段冲突，大多数用户保持默认即可。

## 旁路由用户必读
- 近期不少用户修改配置文件中的默认ip地址，误认为这个工作流可以直接设置旁路ip地址。
- 旁路的逻辑是单网口模式，根据上述的固件属性可知：单网口默认采取 `dhcp模式` 。
- 用户应当自行在上一级路由器查看给`ImmortalWrt`分配的ip地址，然后通过该ip来<br>访问`ImmortalWrt`的后台页面，根据自己主路由的网段，自行配置旁路网关的ip地址。


## 🌟鸣谢
### https://github.com/immortalwrt

