openwrt软路由配置流程

1.固件版本 ImmortalWrt 24.10.0 r32824-6a73dae98c9c / LuCI openwrt-24.10 branch 25.017.24510~d42ec55
下载地址：https://firmware-selector.immortalwrt.org/
2.Nikki插件地址：https://github.com/nikkinikki-org/OpenWrt-nikki
3.ssh连接路由器后台输入以下指令
添加curl指令工具，curl安装命令：
opkg update && opkg install curl
添加nikki插件源：
curl -s -L https://github.com/nikkinikki-org/OpenWrt-nikki/raw/refs/heads/main/feed.sh | ash
下载nikki指令：
opkg install nikki
opkg install luci-app-nikki
opkg install luci-i18n-nikki-zh-cn
4.安装完成后ssh进文件夹
/etc/config/
将nikki、firewall、dhcp文件复制替换掉原文件
5.进入路由器后台-服务-Nikii插件
上传配置文件config.yaml
6.启动
