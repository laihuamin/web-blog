### 概念解析
- 协议
> 不同的硬件、操作系统之间的通信，所有的这一切都需要一种规则，这种规则即为协议
- TCP/IP
> TCP/IP是互联网相关的各类协议的总称，总有人认为这是TCP和IP两种协议是❌的
- 协议族的分成管理
> TCP/IP协议族划分成以下4层：应用层、传输层、网络层和链路层
- 应用层
> 应用层决定了向用户提供应用服务时通信的活动，TCP/IP协议族内预存了各类通用的应用服务，如FTP、DNS、HTTP
- 传输层
> 传输层对上层应用层，提供处于网络连接中的两台计算机的数据传输，有两种不同的协议：TCP和UDP
- 网络层
> 网络层用来处理在网络上的流动的数据包(网络传输的最小数据单元)，该层规定了通过怎样的路径到达对方计算机，将数据传过去
- 链路层
> 用于处理连接网络的硬件部分。硬件上的范畴均在链路层的作用范围之内
- 流程图描述传输过程
![image](https://user-images.githubusercontent.com/28126886/30813627-8e7d17a6-a1d3-11e7-8fc4-4a85e78d04a5.png)
- IP协议
> IP是一个协议的名称和IP地址不同，作用是把各种数据包传送给对方，保证把数据传送给对方需要两个重要条件IP地址和MAC地址
- IP地址
> IP地址指明了节点被分配到的地址
- MAC地址
> 网卡所属的固定地址
- ARP协议
> ARP是一种解析地址协议，可以根据IP地址就可以反查出对应的MAC地址，举个例子，当统一局域网内的两台及其需要通信时，发送端先发出ARP信号，当所属的MAC机器接收到之后，会回一个ARP信号，两台机器通信成功
- 字节流服务
> 字节流服务由位于传输层的TCP协议提供，为了方便传输，将大块数据分割成以报文段为单位的数据包进行传输
- 三次握手
> 握手过程中使用TCP标志——SYN和ACK，流程图如下：
![image](https://user-images.githubusercontent.com/28126886/30815663-6ba3d0ac-a1d9-11e7-9c81-5e2e7784e614.png)
> 当中间过程中断时，TCP协议会以相同顺序发送相同的数据包
- DNS
> 他提供域名到IP地址之间的解析服务，从域名查IP地址或者IP地址查域名的服务
