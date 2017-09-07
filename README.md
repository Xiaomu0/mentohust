# Mentohust
A fork of hyrathb/mentohust dealing with SCAU network

现在 updateing 实现了一个加载支持修改数据包内容的 EAPOL 认证客户端 [MiniEAP](https://github.com/updateing/minieap) 并将本工程的认证算法做成了插件，更加容易适配各个学校，建议大家尝试。

## 使用方法
### 编译
1. 获取源代码
  ```$ git clone https://github.com/Xiaomu0/mentohust.git```
2. 编译
  ```$ cd mentohust && ./autogen.sh && ./configure && make```

### 运行
1. 首先切换到可执行文件所在目录（以下所有操作省略此说明）
  ```$ cd ./src```

2. 运行（需要 root 权限）
  ```$ sudo ./mentohust -uUsername -pPassword```（首次运行会把参数保存到配置文件）

### 退出
不以后台模式运行 mentohust 时，按 Ctrl + C 即可退出，后台运行时使用 ```$ sudo ./mentohust -k``` 退出认证。

### 获取帮助
+ 查看帮助信息请输入：```./mentohust -h```，修改参数请根据帮助信息操作。
+ 例如修改用户名和密码（保存到配置文件）：```$ sudo ./mentohust -uUsername -pPassword -w```
+ 例如修改用户名和密码（仅对当次认证有效）：```$ sudo ./mentohust -uUsername -pPassword```
+ 更详细的帮助信息请参考：http://wiki.ubuntu.org.cn/锐捷、赛尔认证MentoHUST

## 权责声明
1. 本程序所有涉及锐捷赛尔认证的功能均是来自前辈公开代码及抓包分析。
2. 想在本程序于个人仅供学习，于他人仅供方便认证，不得使用本程序有意妨害锐捷赛尔认证机制及相关方利益。
3. 一切使用后果由用户自己承担。
4. 本程序不提供任何服务及保障，编写及维护纯属个人爱好，随时可能被终止。
5. 使用本程序者，即表示同意该声明。谢谢合作。

## 感谢
+ 原 [Hu Yunrui 的 MentoHUST 项目](https://github.com/hyrathb/mentohust) 及为此项目做出贡献者
+ [入山](https://github.com/ShanQincheng) 及其 [教程](http://codingstory.com.cn/mo-gai-mentohust-v4ban-ben-de-xin-de/)
