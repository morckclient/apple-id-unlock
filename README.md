# Morck Apple ID Unlock

Morck Apple ID Unlock是一款专为Apple ID量身定做的自动解锁服务程序，采用苹果接口&Selenium组合的方式实现，可在数秒内完成解锁、解双重认证、改密码等操作，有着极高的解锁效率和便捷的操作。
免搭建运行环境，一键启动web环境。

演示Demo网站

 * https://appleid.morck.xyz     访问密码：morck

## 支持设备

 * Linux（Debian9,10,11）
 * ~~Windows (Windows7,10,11)~~ 暂未发布
 
## 快速开始

初次使用安装chromium（自动删除账号中的登录设备使用chromium操作）

     apt-get update && apt-get install -y chromium chromium-driver
    
下载文件

    wget https://github.com/morckclient/apple-id-unlock/releases/download/v20221108/Morck_Appleid_Unlock_For_Linux_v1.0.31_debug.tar.gz
    
解压&运行

    tar zxvf Morck_Appleid_Unlock_For_Linux_v1.0.31_debug.tar.gz && cd id_unlock && chmod +x unlock && ./unlock -s 管理员密码
    
## 进程守护

    可以使用 `systemd` `Supervisor` `screen` 
    
## 购买许可

 * [Telegram](https://t.me/morck_hh)
