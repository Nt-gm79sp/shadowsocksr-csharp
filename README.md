ShadowsocksR for Windows (Lite)
=======================

- Lite版仅仅只是移除了一些功能，作为命令行与完整版的折衷，以便于在一些奇怪的环境下使用
- **Lite版没有添加任何新功能、算法**
- 对于一般用户，请使用[完整的 ShadowsocksR][SSR]

* This is just a trimmed version of ShadowsocksR for Windows. It is intended for using in specific circumstances, other than Commanand-Line.
* **It has nothing to do with new features or algorithms.**
* For general users, please use the [Full Version of ShadowsocksR for Windows][SSR].

#### 改动

请注意，这些改动对程序性能没有任何提升，仅仅是减少了功能：

1. 裁剪了二维码扫描功能
1. 裁剪了自动更新功能
1. 裁剪了服务器订阅功能
1. 裁剪了客户端密码功能
1. 裁剪了自动运行功能
1. 更换图标为SS蓝色小飞机
1. 单击小飞机图标可以切换全局／PAC两种模式，其它情况不受影响
1. 目标框架为.NET Framework 4.7

（不建议新用户直接使用，建议配合设置好的 gui-config.json 文件使用）

#### Changes

Please note, that these chages have no effect on performance.

1. Trimmed QRCode functions.
1. Trimmed Auto-Updater.
1. Trimmed Server Subscriber.
1. Trimmed Client-configuration-file password-encryptor.
1. Trimmed AutoRun on boot.
1. Legacy-style icons.
1. Click on tray-icon now swap between PAC / Global mode (does not affect Direct mode).
1. Build target .NET Framework 4.7.

You may want to use your original gui-config.json file to ease your configuration.

#### 待解决

1. 解决Windows防火墙报警问题：
既然防火墙阻拦后依然可以正常使用基本功能，就应该有办法不触发防火墙警报，这是Lite版的初衷之一（但好像掉坑里了）
1. 任务栏图标的上传下载提示（来自SS）
1. 将日志窗口与服务器连接统计窗口合并，并导入SS的折线图

以上特性虽然来自[Shadowsocks for Windows][SS]，
但目前SS与SS-R的Win客户端有太多差异，需花时间学习理解两者的诸多不同。
个人能力有限、精力有限，未能利用现有框架做调整，深表遗憾

#### To-do

1. Figure out Windows Firewall warnings.
1. Tray icon display uploading and downloading status (import from SS).
1. Combine Log and ServerLog forms (import from SS).

Although features above are included in [Shadowsocks for Windows][SS], 
it takes time to figure out the differences between SS and SSR. 
Shame on me that I can not re-invent wheels, grrrr...

#### 下载

- 使用 [7-Zip] 解压
- 建议进行 SHA-256 文件指纹校验，方法：安装 [7-zip] 后，右键点击文件 > **CRC SHA** > **SHA-256**
- 如果程序不能运行，需安装最新的 [.NET Framework][NDP]

#### Download

- You will need to download and install [7-Zip] in order 
to extract the ShadowsocksR archive.
- _Optionally_, right-click on the downloaded 7z file and select 
**CRC SHA** > **SHA-256**. Verify that the SHA-256 checksum displayed 
matches the expected checksum which was shown on the releases page.
- Right-click on the downloaded 7z file and do **7-Zip** > **Extract Here** 
or extract to a new folder.
- You may want to [download latest .NET Framework from Microsoft.com][NDP]
if you encountered RUNTIME ERROR.

#### Usage

1. Find ShadowsocksR icon in the notification tray
2. You can add multiple servers in servers menu
3. Select Enable System Proxy menu to enable system proxy. Please disable other
proxy addons in your browser, or set them to use system proxy
4. You can also configure your browser proxy manually if you don't want to enable
system proxy. Set Socks5 or HTTP proxy to 127.0.0.1:1080. You can change this
port in Global settings
5. You can change PAC rules by editing the PAC file. When you save the PAC file
with any editor, ShadowsocksR will notify browsers about the change automatically
6. You can also update the PAC file from GFWList. Note your modifications to the PAC
file will be lost. However you can put your rules in the user rule file for GFWList.
Don't forget to update from GFWList again after you've edited the user rule
7. For UDP, you need to use SocksCap or ProxyCap to force programs you want
to proxy to tunnel over ShadowsocksR

#### Develop

Visual Studio Community 2017 is recommended.

#### License

GPLv3

BreakWa11 has the copyright of ShadowsocksR, which was forked from Shadowsocks by clowwindy.

[SSR]:   https://github.com/shadowsocksrr/shadowsocksr-csharp/releases
[SS]:    https://github.com/shadowsocks/shadowsocks-windows/
[7-Zip]: http://www.7-zip.org/
[NDP]:   https://www.microsoft.com/net/download/thank-you/net471