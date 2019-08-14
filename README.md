# linux_multiply_ips

https://www.laozuo.org/12736.html
<br>

# 方法一：
切换到root用户，编辑 /etc/network/interfaces <br>
照着eth0的样式添加。 <br>
同一网卡就是eth0:1的格式 <br>

# 方法二
命令行法 <br>
sudo ifconfig eth1:1 ip netmask 掩码 <br>
这个方法在unbuntu重启后不能保存，centos重启后可以保存 <br>
用 ip addr  查看网络ip设置情况 <br>


