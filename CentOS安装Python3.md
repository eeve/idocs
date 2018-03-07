# CentOS7安装Python3与Python2共存


> 注意事项

> 1、非root帐号加上sudo

> 2、centos7自带Python 2.7.5是不能卸载的，很多系统级软件依赖这个

## 安装依赖

```
yum -y groupinstall "Development tools"
yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel
```

## 下载python3

```
wget https://www.python.org/ftp/python/3.4.2/Python-3.4.2.tgz
mkdir /usr/local/python3 
tar -zxvf Python-3.4.2.tgz
cd Python-3.4.2
./configure --prefix=/usr/local/python3
make && make install
ln -s /usr/local/python3/bin/python3 /usr/bin/python3
-- 创建Pip3的软链接
ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3 
```

## 测试

```
-- 查看版本
# python3
Python 3.4.2 (default, Jul 19 2016, 03:47:32) 
[GCC 4.8.5 20150623 (Red Hat 4.8.5-4)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

## 代码测试

在当前目录新建个 Python 脚本 hello.py

输入内容

```
!/usr/bin/python3
# 第一个注释
print ("Hello, Python3!") 
```

执行

`python3 hello.py`

-> Hello, Python3!