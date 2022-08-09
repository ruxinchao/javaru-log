# javaru-log
通过web页面展示所有服务的日志，可搜索可暂停
### 演示地址
http://leyao521.cn:81/
### 目录
```
├─javaru-log
│  │  
│  ├─bin----------------启动脚本
│  │ 
│  ├─conf-----------------配置信息
│  │ 
│  ├─logs-----------------日志
│  │ 
│  ├─webapp---------------所需jar
│
```
### 环境
```
jdk 版本：1.8
```
### 开发
```bash
   ## linux
     启动：./bin/javaru-log start
     关闭：./bin/javaru-log  stop
     重启：./bin/javaru-log restart
   ## window（powershell）
     ./bin/javaru-log console
   ## 浏览器访问: 
     http://localhost:82
```
## 配置（conf/application.yml）
    server:
      port: 82  部署端口
    host: 121.43.8.1  部署的服务器真实IP
    name: javaRu-Log  
    logs:
      - name: nginx
        ip: 121.42.8.200  日志所在机器IP
        userName: root 日志所在机器账号
        passWord: xxxxx 日志所在机器密码
        path: /var/log/nginx/access.log   日志所在机器的绝对路径
### 使用说明
``` 
    ## 键盘按键
     S 键：开启
     D 键：暂停
     F 键：高亮关键词
``` 
### 功能截图
![image](https://user-images.githubusercontent.com/60872458/183573719-b015c97d-6171-4a9f-9d38-1bf2c6cb48f6.png)


