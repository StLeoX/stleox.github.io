> 好久没更博客了，好罪恶。
> 
> 前段时间主要是做了一些数据库相关的工作，MiniOB、BusTub之类的项目，然后读了读论文。
> 
> 然后忽然发现自己已经在vanessa上工作了大约一个月了，不禁有感而发，整理一些使用LinuxMint的技巧。

## UI美化

  我的宗旨是能入眼就行，所以这部分的内容没有！！

## 数据管理

  建立了一个远程仓库存放信息：dotfiles、env、apt、pip。通过`cron`每日推送备份。

## 应用管理

### 大型应用

  拒绝flatpak格式的软件包，因为太占体积。

  部分软件使用了Appimage格式，主要因为：1.无其他可选格式；2.该软件更新频繁（例如Workflowy），因为AppimageLauncher能辅助检查更新。

  用了很多 Electron开发的软件，包括：YesPlayMusic/MarkText/Obsidian/wemeet/ 等。

### 小型应用

  Unix下的命令行工具确实很多很好用，~~不好用的也可以自己改造嘛~~。

  例如我现在用到的：

- ls -> exa

- rm -> safe-rm

- cat -> bat

- grep -> ripgrep

- find -> fd

- diff -> delta

- fx: json viewer

- mdv: markdown viewer

- fzf: fuzzy finder

- unar: all-in-one unzipper



## 编程开发

  转向Linux的一大初衷当然是便于C++相关的开发，以及Unix环境下的编程。事实证明，确实很便利，同等硬件下同版本的CLion的速度更快了（当然也有OS的赋能）。

### 公共程序库

  众所周知，apt是C++的包管理器。所以需要什么公共库（狭义理解为apt安装的库）直接apt安装即可。对于**非最新版本**我也可以接受，因为我认为公共库的最新版本就是发布到apt时的版本。目前还未在版本这件事上翻过车。

  之前接触到`topgrade`这款工具，号称是顶级的更新管理工具，后期可以配置下。

### 用户程序库

  其实促使我**在今天**写这篇帖子的一个原因是发现了`stow`这个管理工具。需要库时，它能使用户程序库和公共程序库一样便于搜索和管理；不需要库时，它能帮助开发者一键卸载用户程序库！

> [ref](https://sarcasm.github.io/notes/tools/stow.html)

  基本原理就是将用户程序库的全部内容置于`/usr/local/stow/`下，然后在外部建立符号链接（如在`/usr/local/bin/`下建立指向BIN文件的链接）。












