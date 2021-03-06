*配置文件注释*

- <dubbo:service/> 服务配置，用于暴露一个服务，定义服务的元信息，一个服务可以用多个协议暴露，一个服务也可以注册到多个注册中心。
- <dubbo:reference/> 引用配置，用于创建一个远程服务代理，一个引用可以指向多个注册中心。
- <dubbo:protocol/> 协议配置，用于配置提供服务的协议信息，协议由提供方指定，消费方被动接受。
- <dubbo:application/> 应用配置，用于配置当前应用信息，不管该应用是提供者还是消费者。
- <dubbo:module/> 模块配置，用于配置当前模块信息，可选。
- <dubbo:registry/> 注册中心配置，用于配置连接注册中心相关信息。
- <dubbo:monitor/> 监控中心配置，用于配置连接监控中心相关信息，可选。
- <dubbo:provider/> 提供方的缺省值，当ProtocolConfig和ServiceConfig某属性没有配置时，采用此缺省值，可选。
- <dubbo:consumer/> 消费方缺省配置，当ReferenceConfig某属性没有配置时，采用此缺省值，可选。
- <dubbo:method/> 方法配置，用于ServiceConfig和ReferenceConfig指定方法级的配置信息。
- <dubbo:argument/> 用于指定方法参数配置。

*缺省主机端口与协议相关：*

- dubbo: 20880
- rmi: 1099  *(RMI全称是Remote Method Invocation－远程方法调用，Java RMI在JDK1.1中实现的，其威力就体现在它强大的开发分布式网络应用的能力上，是纯Java的网络分布式应用系统的核心解决方案之一。其实它可以被看作是RPC的Java版本。但是传统RPC并不能很好地应用于分布式对象系统。而Java RMI 则支持存储于不同地址空间的程序级对象之间彼此进行通信，实现远程对象之间的无缝远程调用。)*
- http: 80
- hessian: 80
- webservice: 80
- memcached: 11211
- redis: 6379
