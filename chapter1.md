# 复习题
## 1.1 
1. 主机与端系统相同
2. none
3. 标准确定了报文的数据格式,发送和接收报文时所采取的动作,在发送接收双方标准一致时,才能完成有效的通信
## 1.2
4. DSL,同轴电缆,FTTH,拨号卫星,以太网,WIFI.
- 住宅:DSL,同轴,FTTH,偏远地区用卫星.
- 公司接入:一般是以太网和wifi
- 广域无线网:3G和LTE
5. HFC是 用户间 用 同轴电缆, 到ISP是走的光纤.所以用户间是共享的,下行信道也可能碰撞.
6. None
7. 以太LAN传输速率:用户:100Mbps-1Gbps,服务器:1Gbps-10Gbps
8. 运行以太网的物理媒体:以太网专指有限局域网吧,那就是用双绞线.
9. DSL:专用,55Mbps下行,15Mbps上行<br>
    HFC:共享,DSL,42.8Mbps下行,30.7Mbps<br>
    拨号调制解调器:专用,56Kbps<br>
    FTTH:专用.可达每秒上千兆bps
10. None
## 1.3
11. 总时延: L/R1 + L/R2
12. 电路交换网络相比分组交换网络更适合实时服务.TDM适合数字信号传输,FDM适合模拟型号传输
13. a. 两个
    b. 信道最大就2Mbps
    c. 20%
    d. 0.2^3. 三个1Mpbs的话,就是队列以1M/s的速率增长.
14. 为了减少客户ISP向供应商ISP提供的流量费用,直接将他们的网络连在一起, IXP(因特网交换点)就是实现对等的节点,大概就是收取服务费之类的赚钱
15. 谷歌在全球各地搭服务器和比较低的ISP对等(接IXP或者直接连低层ISP),绕过高层的ISP,实在不行再走一层的ISP,这样既减少了流量费用,还增加了对于服务如何交付给用户的控制.
## 1.4
16. 端到端的时延组成部分有:排队时延,传输时延,传播时延,处理时延. 其中固定的是传输传播和处理<br>
    $d_{end-end} = N(d_{proc}+d_{trans}+d_{prop})$ 在各节点具有不同时延和每个节点存在平均排队时延时,要对上式进行一般化处理.
17. None
18. $cost=1000*8/(2*10^8)+2500*10^3/(2.5*10^8)$<br>
    $cost=L/R+d/s$ 该时延与传输速率有关
19. a. 500kbps<br>
    b. 4MB/500kbps<br>
    c. 速率减少为100kbps,计算类似
20. 端系统在分组的首部加上目标端的ip地址,当一个分组到达网络中的路由器时,路由器检查该分组的目的地址中的一部分,向一台相邻路由器转发该分组.(每台路由器有一份<b>转发表</b>,用于将目的地址(或其一部分)映射称输出链路.当某分组到达一台路由器时,路由器检查该地址,并用这个目的地址搜索其转发表,以发现适当的输出链路,将分组转发至该链路上)
21. None
## 1.5
22. 错误控制、流量控制、分段、重组、复用、连接设置等等。是的，比如错误控制会有多个层次执行。
23. 应用层,运输层,网络层,链路层,物理层.
    - 应用层:报文,应用程序--应用程序
    - 运输层:报文段,应用程序端口--应用程序端口
    - 网络成:数据报,主机----主机
    - 链路层:帧,网络节点---网络节点(路由器,交换机,主机)
    - 物理层:比特,节点---节点(将帧中的一个个比特从一个节点移动到下一个节点)
24. - 应用层报文:一个端系统中的应用程序使用  协议 与另一个端系统中的应用程序  交换信息的分组叫做应用层报文.
    - 运输层报文:使用TCP或者UDP协议  对应用层报文进行封装 所得到的 分组
    - 网络层数据包: 封装运输层报文
    - 链路层帧:封装数据包
25. 路由器处理  网络层,链路层,物理层. 交换机处理链路层和物理层.主机处理五个层次

