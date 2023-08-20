# EmbyCrack_Windows

利用 Nginx 反代理实现 emby 高级会员解锁

当前使用 Nginx 版本为稳定版 1.24.0



1.安装证书GMCert_RSACA01并添加到受信任

证书服务端、客户端均需安装（证书在程序目录下）
`GMCert_RSACA01.cer` `GMCert_RSACA01.cert` 为同一证书，windows 安装 cer 后缀即可



2.双击 start.bat 或 nginx.exe 启动服务



3.在路由器设置 hosts 或修改本地 hosts

在 hosts 文件中添加的内容：`本机ip mb3admin.com` 

iOS、iPadOS 在未越狱状态下仅能通过路由器 hosts 或利用小火箭、圈 x 等工具解锁



4.在 emby 控制台随意输入激活码进行激活



可输入以下网址进行验证：

`https://mb3admin.com/admin/service/registration/validateDevice`

返回以下信息即成功

`{"cacheExpirationDays": 365,"message": "Device Valid","resultCode": "GOOD"}`



双击 stop.bat 停止运行 
