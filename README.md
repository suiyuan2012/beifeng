SSH连接正常机器



lsblk 或 fdisk -l查看附加卷





安装后台工具

apt update -y && apt install -y tmux

tmux new -s my1

tmux attach-session -t my1





下载与恢复

ubuntu18.04 ARM 官方原版完整救援包（用户名：root , 密码：CNBoy.org） 

wget --no-check-certificate https://github.com/honorcnboy/BlogDatas/releases/download/OracleRescueKit/ubuntu18.04.arm.img.gz 

gzip -dc /root/ubuntu18.04.arm.img.gz | dd of=/dev/sdb





ubuntu18.04 AMD 官方原版完整救援包（用户名：root , 密码：CNBoy.org） 

wget --no-check-certificate https://github.com/honorcnboy/BlogDatas/releases/download/OracleRescueKit/ubuntu18.04.amd.img.gz 

gzip -dc /root/ubuntu18.04.amd.img.gz | dd of=/dev/sdb





debian10 ARM 网络精简救援包（用户名：root , 密码：10086.fit） 

wget --no-check-certificate https://github.com/honorcnboy/BlogDatas/releases/download/OracleRescueKit/dabian10.arm.img.gz 

gzip -dc /root/dabian10.arm.img.gz | dd of=/dev/sdb

.

制作自己的救援包

将健康的引导卷分离挂载到账号下任意可用机器上，上机器输入以下命令！

dd if=/dev/sdb | gzip > /root/own.img.gz


