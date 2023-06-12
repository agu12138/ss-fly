一键脚本安装shadowsocks/shadowsocksR/V2Ray + 开启bbr
---

一键脚本搭建shadowsocks/shadowsocksR/V2Ray + 设置开启自启动 + 升级内核&开启bbr加速。
---

# SS

# 安装
ss-fly/ss-fly.sh -i password port

# 修改配置文件
vim /etc/shadowsocks.json

#停止服务
ssserver -c /etc/shadowsocks.json -d stop

# 启动服务
ssserver -c /etc/shadowsocks.json -d start

# 重启服务
ssserver -c /etc/shadowsocks.json -d restart

# 卸载ss服务
ss-fly/ss-fly.sh -uninstall

---
# SSR 

# 安装
ss-fly/ss-fly.sh -ssr

# 启动服务
/etc/init.d/shadowsocks start

# 停止服务
/etc/init.d/shadowsocks stop

# 重启服务
/etc/init.d/shadowsocks restart

# 查看状态
/etc/init.d/shadowsocks status

# 卸载SSR服务
./shadowsocksR.sh uninstall
 
# 配置文件路径
/etc/shadowsocks.json

# 日志文件路径
/var/log/shadowsocks.log

# 代码安装目录
/usr/local/shadowsocks