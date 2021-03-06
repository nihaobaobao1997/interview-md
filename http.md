## http https 有什么区别
* http 是明文传输，没有安全保证，对服务端和客户端来说都无法验明双方身份
* https 使用了ssl加密方式，服务端和服务端可以验明双方的身份，安全有了一定的保障。但是需要解密和加密，对性能会造成一定的影响。
* http端口号是80 ，https端口号是443。

## TCP三次握手
1. 为什么： 
	* 需要三次握手才能确认双方的接收与发送能力是否正常。
2. 怎么办：
	* 第一次握手：客户端发送网络包，服务端收到了。 这样服务端就能得出结论：客户端的发送能力、服务端的接收能力是正常的。 
	* 第二次握手：服务端发包，客户端收到了。 这样客户端就能得出结论：服务端的接收、发送能力，客户端的接收、发送能力是正常的。
		ps：不过此时服务器并不能确认客户端的接收能力是否正常。
	* 第三次握手：客户端发包，服务端收到了。 这样服务端就能得出结论：客户端的接收、发送能力正常，服务器自己的发送、接收能力也正常。


## DNS是什么？你了解过DNS吗？
1. DNS是域名系统，是应用层的一个协议。我们通常是通过DNS去解析域名获取IP，根据IP去向服务端发送数据请求的。
2. DNS也是一个分布式的数据库，正是因为DNS的缓存机制，我们可以很快地知道域名对应的IP地址，从而更快的获取连接。

## 你了解nginx吗？
* 特性：
	1. 正向代理
	2. 反向代理
		* 将请求在内部进行IP转化，发送到对应的服务器上，也可能是同一台服务器，端口号不同。安全性更高，不易被捕获服务器的IP地址。
	3. 负载均衡
		* 负载均衡也是nginx最常用的一个功能，如果请求过多的时候，将不同的请求发送不同的服务器，避免因为服务器处理请求过慢，导致的响应数据的问题。

## 知道CDN吗？说一下CDN
1. 是什么？
	* CDN是构建在现有网络基础之上的智能虚拟网络，依靠部署在各地的边缘服务器
2. 干什么？
	* 使用户就近获取所需内容，降低网络拥塞，提高用户访问响应速度和命中率。

## 