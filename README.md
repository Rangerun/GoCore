# GoCore

## 基于服务设计的web框架

### 怎么添加一个服务

新增三个文件

* contract.go 里面放置服务的凭证和接口协议和一些需要用到的数据结构
* provider.go 因为需要遵循框架容器协议，服务提供方需要实现特定的接口
* service.go 里面是contract.go接口的具体实现，并为provider.go里的注册方法提供服务初始化

然后再main中绑定服务后，在路由文件route.go中获取注册的实例进行使用
