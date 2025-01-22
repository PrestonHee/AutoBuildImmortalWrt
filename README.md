# AutoBuildImmortalWrt

## 🤔 这是什么？
它是一个工作流。可快速构建 带docker且支持自定义固件大小的 immortalWrt
> 1、支持自定义固件大小 默认1GB <br>
> 2、支持预安装docker（可选）<br>
> 3、目前支持x86-64 和 rockchip 两个平台（后续会增加）<br>
> 4、新增支持MT3000/MT2500/MT6000/B2200（docker可选）<br>
> 5、新增全志平台R1S、香橙派Zero3等机型的工作流<br>
> 6、新增用户预设置pppoe拨号功能<br>
> 7、新增树莓派①②③④⑤<br>
## 如何查询都有哪些插件?
https://mirrors.sjtug.sjtu.edu.cn/immortalwrt/releases/23.05.4/packages/aarch64_cortex-a53/luci/ <br>
https://mirrors.sjtug.sjtu.edu.cn/immortalwrt/releases/23.05.4/packages/x86_64/luci/ 

## 该固件默认属性？(必读)
- 该固件刷入单网口设备默认采用DHCP模式,自动获得ip。类似NAS的做法
- 该固件刷入多网口设备默认WAN口采用DHCP模式，LAN 口ip为 192.168.100.1
- 综合上述特点，单网口应该先接路由器，先在路由器查看一下它的ip 再访问。
- 上述特点 你都可以通过 `99-custom.sh` 配置和调整


## ❤️如何构建docker版ImmortalWrt（建议收藏）⬇️
https://wkdaily.cpolar.top/15
# 🌟鸣谢
### https://github.com/immortalwrt
