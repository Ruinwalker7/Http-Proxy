# HTTP代理

### 如何运行
**编译：**
```
mkdir build
cd build
cmake ..
make .
```
**运行：**
```
./proxy <端口号>
```
例子：
```
./proxy 8080
```

### 测试
在一个新的终端中：
```
telnet localhost 8080
GET http://www.baidu.com/ HTTP/1.0
SET http://www.baidu.com/ HTTP/1.0
```
只支持get请求，其他请求会返回错误501