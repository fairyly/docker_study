# error during connect: Get http://%2F%2F.%2Fpipe%2Fdocker_engine/v1.37/version: 


windows 10 家庭版

>open //./pipe/docker_engine: The system cannot find the file specified.   
In the default daemon configuration on Windows, the docker client must be run elevated to connect.   
This error may also indicate that the docker daemon is not running.  




## 解决：

打开新窗口后执行
```
@FOR /f "tokens=*" %i IN ('docker-machine env default') DO @%i

default 是docker-machine的name，可以通过docker-machine -ls 查看


又根据提示创建 machine
```

