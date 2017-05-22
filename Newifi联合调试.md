## 相关程序及策略说明
1. pear_restart死活程序
> 负责监控pear_software中所有程序的健康运行

2. pear_monitor终端监控程序
>  获取PLATFORM平台架构信息，公网ip，本地ip，mac地址，hardware相关信息
>  配置nginx，包括动态申请http端口，和https端口
>  五分钟定时执行测速和远程升级的功能

3. pear_nginx
>  提供http/https(tcp)数据传输通道 

4. pear_datachannel
>  提供webrtc datachannel(udp)数据传输通道 

## 关于存储空间的说明

 pear_monitor定时检测设备外接硬盘设备，永远选择容量最大的设备分区，目前配置为需要10G以上的缓存空间：
 > 缓存空间=硬盘可用空间+硬盘下已经缓存的空间
 
## 需Newifi集成事宜及API
   1. Newifi把下面文件集成到路由器中，设置开机启动pear_restart即可：
   * /usr/sbin/pear_monitor
   * /usr/sbin/pear_restart(会负责启动相关服务)
   * /usr/sbin/pear_nginx
   * /etc/pear_restart/.conf.json
   > 现有服务或新添加的服务，后续会直接通过远程升级的方式fix bug 或者增加新的服务，以保证服务的稳定和持续增值的能力
   
   2. 提供服务器端查询接口，查询mac与sn的有效性接口


