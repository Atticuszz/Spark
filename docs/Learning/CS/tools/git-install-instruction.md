# Git-install-instruction

note: 转自 [知乎](https://zhuanlan.zhihu.com/p/473593640) 加了一点注释，_使用斜体_
![](https://pic1.zhimg.com/80/v2-1e31c0a222573e8d2465e1bc1de15a3c_720w.webp)

根据自己电脑系统下载相应的安装包
_现在电脑一般是 64 位的_

## 1）许可申明

![](https://pic1.zhimg.com/80/v2-da7b6da5dcf23ff74712a09fae1fe8f4_720w.webp)

点击 “Next” 即可。

## 2）选择安装路径

![](https://pic2.zhimg.com/80/v2-7023d4e68bd7ea15e42c6ad0d711d685_720w.webp)

根据自己需要修改安装位置。

## 3）选择安装组件

![](https://pic2.zhimg.com/80/v2-820dcc02ca01bdf8cf70477a3d8fc459_720w.webp)

a) 默认勾选的选项，建议不要动。默认安装了一些组件 Git Bash ,Git GUI 以及 Git LFS 还有桌面快捷方式以及配置文件默认的文本编辑，使用 sh 脚本启动 git bash.

b) 红色框框决定在所有控制台窗口中使用 TrueType 字体和是否每天检查 Git 是否有 Windows 更新，按需勾选。

注：Git LFS 用于实现 Git 对大文件的支持 ，LFS 策略可以节省存储空间和提高性能，比如游戏开发中设计资源文件占用很大。

## 4）选择开始菜单目录

![](https://pic2.zhimg.com/80/v2-a8613a8cff0959ea103888ee8fa107b9_720w.webp)

默认 git 即可 直接 next。

## 5）选择 Git 文件默认的编辑器

![](https://pic1.zhimg.com/80/v2-9c0b533d485a0a48d8fa9672d2f1dd78_720w.webp)

很少用到，所以默认 Vim 即可，直接点“Next”。

## 6）选择 Git 初始化分支的名称

![](https://pic2.zhimg.com/80/v2-d801081a48de96c214602e424e239f55_720w.webp)

a) git 默认的初始化分支名称为 "master"。

b) 根据自己项目业务重新命名 如：main,trunk 或者自己填写。

注：已经存在的项目不受影响。

## 7）选择使用 Git 的方式

![](https://pic4.zhimg.com/80/v2-81f001420be540250340e1d09067366f_720w.webp)

a) 第一个选项, 只从 Git Bash 命令行工具 使用 Git，也是最谨慎的默认的选择。

b) 第二个选项, 从命令行或者第三方软件 使用 Git。
_肯定选第二个，以后会遇到 win+r 打开 cmd(命令行工具)，powershell(win 加强版 cmd) 使用 git 命令，而且也会与 pycharm 这种 IDE(集成开发环境结合在一起)_
c) 第三个选项，在命令提示符中使用 Git 和可选的 Unix 工具。

注：这三个选项 我也有点迷 不知什么场景会用到，有啥用，希望有知道的大神回复告知下。

## 8）选择 Https 传输后端

![](https://pic4.zhimg.com/80/v2-a40449d69c0eb85581e675c1f672022b_720w.webp)

让 Git 使用哪个 SSL/TLs 库来进行 HTTPS 连接?

a) 第一个选项，使用 OpenSSL 库，服务器 cer 证书将使用 ca 包中.crtw 文件进行验证通过，默认选这个。

b) 第二个选项，使用本机 Windows 安全通道库，服务器证书将在 Windows 证书存储中进行验证。这个选项还允许您通过 Active Directory 域服务使用您的公司内部根 CA 证书。

## 9）配置结束行转换方式

![](https://pic2.zhimg.com/80/v2-d045cb53a0315a4dcea38adf569a95cd_720w.webp)

Git 应该如何处理文本文件中的行结尾?

a) 第一个选项，下拉是转换 Windows 风格，提交转换为 iunix 风格，在 windows 这是推荐默认的设置。

b) 第二个选项，下拉时不改变，提交转换为 iunix 风格。对于跨平台项目，这是 Unix 上的推荐设置。

c) 最后一个选项，下拉和提交都不进行任何转换，对于跨平台项目 (“核心项目”)，不推荐选择此选项。

## 10）配置终端模拟器为使用 Git Bash

![](https://pic4.zhimg.com/80/v2-675b9bf712c47d6a2d45eaf9852f8b13_720w.webp)

a) 第一个选项，Git Biash 将使用 MinTTY 作为终端模拟器，它拥有一个可调整大小的窗口，非矩形的选择和 Unicode 字体。Windows 控制台程序 (如交互式 Python) 必须通过 winpty’启动才能在 MinTTY 中工作，默认选择这个更灵活。

b) 第二个选项，使用 Windows 的默认控制台（cmd.exe）,它可以在 Win32 控制台程序中工作，如交互式 Python 或 node。is，但有一个非常有限的默认滚动回滚，需要配置为使用 Unicode 字体，以便正确显示非 ascil 字符，在 Windows 10 之前，它的窗口不能自由调整大小，它只允许矩形文本选择

## 11）选择 Git 下拉默认行为

![](https://pic1.zhimg.com/80/v2-4c67e5d14528cbcce5f00918be3e8a48_720w.webp)

a) 第一个选项，默认 (快进或合并)。这是“git pull”的标准行为: 尽可能快进当前分支到一个被捕获的分支，否则创建合并提交。

b) 第二个选项，将当前分支改为获取的分支。如果没有要重基的本地提交，这相当于快进。

c) 第三个选项，仅仅快进， 快进到获取的分支。如果不可能，就失败。

## 12）选择 Git 凭证小助手

![](https://pic2.zhimg.com/80/v2-85dbfc5c1c19e29f854809bf724d5b31_720w.webp)

Credential helper 是帮我们保存凭证（用户密码）他有很多存储模式如：cache，store，manager 和 osxkeychain，默认 wincred，这里根据自己需要选择。

## 13）配置额外特性选项

![](https://pic1.zhimg.com/80/v2-c75307d42b2abc1b97b08cea7ad719cc_720w.webp)

a) 第一个选项，启用文件系统缓存,文件系统数据将被大量读取，并缓存到内存中以用于某些操作 (“core。fscache" 设置为 "true")。这提供了显著的性能提升。

b) 第二个选项，支持符号链接，启用符号链接 (需要 SeCreateSymboliclink 权限)。请注意，现有存储库不受此设置的影响。

## 14）启用实验配置选项

![](https://pic1.zhimg.com/80/v2-671907fb4ee730b7f55d214926c006b0_720w.webp)

启用对伪控制台的实验性支持,(新) 这允许在 Git Bash 窗口中运行原生控制台程序，如 Node 或 Python，而不使用 winpty，但它仍然有已知的 bug,一般用不到 可不勾选

点击 Install 即可安装完毕。

## 15）安装完成

Git 的安装完成，可以在开始菜单中看到 Git 的三个启动图标（Git Bash、Git CMD(Deprecated)、Git GUI）。
_Deprecated 是不在维护，或者快要废弃掉了_
Git GUI，是 Git 的可视化操作工具，点击打开如下图：

![](https://pic4.zhimg.com/80/v2-8e475844e9f8b035467192b27ffef2a3_720w.webp)

Git Bash，是 Git 配套的一个控制台，点击打开如下图：

![](https://pic2.zhimg.com/80/v2-9b76b24434f23e5f8a173e95d9cd2d85_720w.webp)

Git CMD(Deprecated)，是通过 CMD 使用 Git（不推荐使用），点击打开如下图

![](https://pic2.zhimg.com/80/v2-24b58689d961b592cd01c42d88187821_720w.webp)

_这几个我都不用😂😂😂，pycharm 配置 git，会有图形化界面方便操作，克隆项目一般也都是在 pycharm 里面输入链接直接克隆，实际上现代的开发环境工具几乎都内置结合操作 git 的界面，而不是原始的命令行，但命令行也需要了解一些的，一些细致的配置比如代理（和连接外网有关）的配置，仍然需要命令行_

在终端 clone 仓库时，若出现 don't connect，则需要配置端口信息。
例如你使用的是 Clash，则端口参数默认为 7890.