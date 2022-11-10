# Morck Apple ID Unlock

Morck Apple ID Unlock是一款专为Apple ID量身定做的自动解锁服务程序，采用苹果接口&Selenium组合的方式实现，可在数秒内完成解锁、解双重认证、改密码等操作，有着极高的解锁效率和便捷的操作。
免搭建运行环境，一键启动web环境。


演示Demo网站

 * https://appleid.morck.xyz     访问密码：morck

支持的功能

| 功能                   | 支持 | 说明 |
|-----------------------|------|------|
| 一键检测账号状态        | ✔︎   |      |
| 解除双重认证绑定        | ✔︎   |      |
| 解除账号异常锁定        | ✔︎   |      |
| 密码错误自动更改        | ✔︎   |      |
| 定时删除登录设备        | ✔︎   |      |
| 后台管理面板           | ✔︎   |      |
| 自定义自动解锁时间      | ✔︎   |      |
| 自定义定时删除设备时间  | ✔︎   |      |
| 网站模板自定义          | ✔︎   |      |
| 远程获取账号信息        | ✔︎   |      |
| 限制网站请求次数        | ✔︎   |      |


## 支持设备

 * Linux（Debian9,10,11）
 * ~~Windows (Windows7,10,11)~~ 暂未发布
 
## 快速开始

初次使用务必安装chromium（自动删除账号中的登录设备使用chromium操作）

     apt-get update && apt-get install -y chromium chromium-driver
    
下载文件

    wget https://github.com/morckclient/apple-id-unlock/releases/download/v20221108/Morck_Appleid_Unlock_For_Linux_v1.0.31_debug.tar.gz
    
解压&运行

    tar zxvf Morck_Appleid_Unlock_For_Linux_v1.0.31_debug.tar.gz && cd id_unlock && chmod +x unlock && ./unlock -s 你的管理员密码
    
## 启动参数
    -s  string <必选>
		设置管理员访问密码

	-h string <可选>
		为WEB服务绑定域名

	-p  int <可选>
		服务将在本地地址0.0.0.0运行，默认使用80端口，如果本地启用ssl请使用 443 端口，且需将ssl证书文件 <server.pem> <server.key> 放置到路径下的ssl目录下

	-r  string <可选>
		启用Redis模式，Redis链接示例 `redis://:password@host:port` 限制请求次数记录值默认会使用系统内存记录，可能会造成内存过度消耗并导致系统运行异常，开启redis模式会大大减少系统内存消耗

	-l  <可选>
		关闭api请求次数限制模式，使用反向代理时必选
 
	-d  <可选>
		启用调试模式
 
	--version  输出当前版本号

	--help  输出启动参数说明

    
## 进程守护

可以使用 `systemd` `Supervisor` `screen` 等后台运行

## 调用接口

获取独立账号生成的网页
| URL                            | 请求  | 描述 |
|--------------------------------|------|----------|
| /preview                       | GET  | [说明文档](https://github.com/morckclient/apple-id-unlock/blob/main/api.md#1%E8%8E%B7%E5%8F%96%E7%8B%AC%E7%AB%8B%E8%B4%A6%E5%8F%B7%E7%94%9F%E6%88%90%E7%9A%84%E7%BD%91%E9%A1%B5) |


获取独立账号的JSON
| URL                            | 请求  | 描述 |
|--------------------------------|------|------|
| /getInfo/id                    | GET  | [说明文档](https://github.com/morckclient/apple-id-unlock/blob/main/api.md#2%E8%8E%B7%E5%8F%96%E7%8B%AC%E7%AB%8B%E8%B4%A6%E5%8F%B7%E7%9A%84json) |


获取全部账号的JSON
| URL                            | 请求  | 描述 |
|--------------------------------|------|------|
| /getInfo/all_id                | GET  | [说明文档](https://github.com/morckclient/apple-id-unlock/blob/main/api.md#3%E8%8E%B7%E5%8F%96%E5%85%A8%E9%83%A8%E8%B4%A6%E5%8F%B7%E7%9A%84json) |


    
## 购买许可

 * [Telegram](https://t.me/morck_hh)
