# linux_multiply_ips

https://www.laozuo.org/12736.html
<br>

# 方法一：
切换到root用户，编辑 /etc/network/interfaces <br>
照着eth0的样式添加。 <br>
同一网卡就是eth0:0的格式 <br>
实测中多ip需要有eth0:0 <br>
不能直接跳到eth0:1 <br>

# 方法二
命令行法 <br>
sudo ifconfig eth1:1 ip netmask 掩码 <br>
这个方法在unbuntu重启后不能保存，centos重启后可以保存 <br>
用 ip addr  查看网络ip设置情况 <br>

# 方法三
有人用这样的方法 <br>
iface eth0 inet static<br>
address 192.168.1.1<br>
netmask 255.255.255.0<br>
gateway 192.168.1.254<br>

iface eth0:0 inet static<br>
address 192.168.1.2<br>
netmask 255.255.255.0<br>
gateway 192.168.1.254<br>

iface eth0:1 inet static<br>
address 192.168.1.3<br>
netmask 255.255.255.0<br>
gateway 192.168.1.254<br>


