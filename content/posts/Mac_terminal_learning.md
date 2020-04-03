---
title: "Mac terminal 学习笔记"
date: 2020-04-01T15:05:55+08:00
draft: false
---


终端是连接内核和交互界面的桥梁，通过终端，用户可以间接控制系统内核。命令的组成包括命令对象，修饰命令和命令内容等。

![image](/images/Mac_terminal_learning/command_consist.png) 

# 常见命令

1. 路径分为相对路径和绝对路径。 【/文件夹名/文件夹名】 绝对路径，【./文件夹】 相对路径。
2. pwd 显示当前路径；
3. cd 进入某个文件夹； cd ~回到根目录； cd  .. 回退到上一个文件夹；cd ./文件夹名 进入下一个文件夹。 
	      “~” 也表示为 home 目录 的意思，	”.” 则是表示目前所在的目录，”..” 则表示目前目录位置的上一层目录。
4. ls 显示此路径下所有文件；ls -R 显示当前路径下展开子文件夹的内容(注意是大写R)；
5. clear 清屏
6. man + 指令名查看该指令的用法；q 退出说明。
7. control + c 停止当前进程

# 常见用法
	
1. killall + 应用程序名 强退某个进程
2. caffeinate 让电脑时刻保持清醒
3. touch -t 202003102346 文件绝对路径 更改文件的修改时间(实测发现创建时间和修改时间不同的无法修改)
4. defaults write com.apple.screencapture type jpg 更改截屏的默认格式； defaults write com.apple.screencapture disable-shadow -bool true; killall SystemUIServer
5. defaults write com.apple.finder AppleShowAllFiles -bool true; killall Finder 显示隐藏文件夹
6. defaults write com.apple.dock persistent-apps -array-add ‘{“tile-type”=“spacer-tile”;}’; killall Dock 为dock增加空白dock栏
7. textutil -convert txt 文件名称 ，这句指令允许你将任何文件，在以下文件格式中互相转换 txt, html, rtf, rtfd, doc, docx, wordml, odt, webarchive。
8. mv移动文件；mkdir创建目录；cat显示文件内容
9. echo + something 是在屏幕上打印某些内容 echo ‘* - nofile 65535’ >> /etc/security/limits.conf  will append - nofile 65535### to the end of the /etc/security/limits.conf### file, instead of printing - nofile 65535### on the screen.

### 参考链接
1. [每天一个linux链接](https://www.cnblogs.com/peida/archive/2012/12/05/2803591.html)
2. [玩转Terminal入门](https://sspai.com/post/45534)