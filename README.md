# FinalSpeed
服务器TCP双边加速软件可达到90%的物理带宽利用率

[FinalSpeed官方停止维护更新](http://www.ip4a.com/t/944.html),且行切珍惜！ 


一. 开放端口

service iptables start

iptables -A INPUT -p tcp --dport 你的vps端口号 -j ACCEPT

iptables -A OUTPUT -p tcp --sport 你的vps端口号 -j ACCEPT

service iptables save

二. 安装命令:

rm -f install_fs.sh

wget https://raw.githubusercontent.com/KorudoKyatto/FinalSpeed/master/install_fs.sh

chmod +x install_fs.sh

./install_fs.sh 2>&1 | tee install.log

三. 常用命令使用说明

更新：执行一键安装会自动完成更新。

卸载： sh /fs/stop.sh ; rm -rf /fs

启动： sh /fs/start.sh

停止： sh /fs/stop.sh

重新启动： sh /fs/restart.sh

运行日志： tail -f /fs/server.log

