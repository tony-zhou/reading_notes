# 第一章 Unix/Linux shell简介
## 1.1 Unix与Linux及其历史
### 1.1.1 Unix简介
* 一个多用户、多任务的操作系统

### 1.1.2 为什么选择Linux

## 1.2 shell的定义与功能
### 1.2.1 Unix shell
* Bourne shell
	* `用于系统管理，提示符: $` 
* C shell
	* `提示符: %` 
* Korn shell
	* `Bourne shell的扩展集，提示符: $`

### 1.2.2 Linux的shell
* GNU bash (Bourne Again shell)
	* `提示符: $` 
* TC shell
	* `提示符: >` 
* Z shell
	* `结合了Bourne Again shell、TC shell和Korn shell的许多功能`

## 1.3 shell的历史
### 1.3.1 shell的作用
* 在交互方式下解释从命令行输入的命令
* 定制用户环境，通常在shell的初始化文件中完成
* 解释性编程语言

### 1.3.2 shell的职责
* 读取输入并解释命令行
* 替换特殊字符，比如通配符和历史命令符
* 设置管道、重定向和后台处理
* 处理信号
* 程序执行的相关设置

## 1.4 系统启动与登录shell
 