- http报文的结构

http协议的请求和响应，必须包含的部分是http首部，首部内容为客户端和服务器分别处理请求和响应提供需要的信息

- http请求报文

http请求报文由方法、URI、HTTP版本、HTTP其他首部字段组成

- http响应报文

HTTP报文由HTTP版本、状态码（数字和短语）、HTTP首部字段组成

- http首部字段

在客户端和服务端通信中，无论是请求还是响应，都会使用首部字段，他能起到额外传递信息的效果

- http首部字段的结构

http首部字段是由首部字段名和字段值构成，中间用冒号分隔，首部字段名：字段值，举个例子：
Content-Type：text/html

- http字段重复了会怎么样

出现两个及两个以上相同的首部字段名，规范尚未明确，有些浏览器会以第一个为准，有些浏览器会以后面的字段名为准。
注：我觉得不然，因为以前遇到set-Cookie的时候，出现多个浏览器会正常处理，所以还得看的吧

- http首部字段类型

通用首部字段、请求首部字段、响应首部字段、实体首部字段

- 通用首部字段

请求和响应都会使用的字段

- 请求首部字段

从客户端向服务器发送请求报文时使用的首部字段。补充了请求的附加内容，客户端信息、响应内容相关优先级等信息。

- 响应首部字段

从服务器向客户端返回响应报文时使用的首部。补充了响应的附加内容、也会向要求客户端附加额外的内容信息

- 实体首部字段

针对请求报文和响应报文的实体部分使用的首部。补充了资源内容更新时间等与实体有关的信息

- 通用首部字段一览

| 首部字段名        | 说明                   |
| ----------------- |:----------------------:|
| Cache-Control     | 控制缓存行为           |
| Connection        | 逐跳首部、连接的管理   |
| Data              | 创建报文的时间         |
| Pragma            | 报文指令               |
| Trailer           | 报文末端的首部一览     |
| Transfer-Encoding | 指定报文主题的编码方式 |
| Upgrade           | 升级为其他协议         |
| Via               | 代理服务器的相关信息   |
| Warning           | 错误通知               |
- 请求首部字段一览

| 首部字段名 | 说明 |
| -- |:---:|
| Accept | 用户代理可处理的媒体类型 |
| Accept-Charset | 优先的字符集 |
| Accept-Encoding | 优先的内容编码 |
| Accept-Language | 优先的语言类型 |
| Authorization | Web认证信息 |
| Expect | 期待服务器的特定行为 |
| From | 用户的邮箱地址 |
| Host | 请求资源所在的服务器 |
| If-Match | 比较实体标记(Etag) |
| If-Modified-Since | 比较资源更新时间 |
| If-None-Match | 比较实体标记（与If-Match相反）|
| If-Range | 资源未更新的byte的范围请求 |
| If-Unmodified-Since | 比较资源更新时间（与If-Modified-Since相反） |
| Max-Forwards| 最大传输逐跳 |
| Proxy-Authorization | 代理服务器要求客户端的认证信息 |
| Range | 实体的范围请求 |
| Referer | 对请求中的URI的获取方 |
| TE | 传输编码的优先级 |
| User-Agent | Http客户端程序的信息 |

