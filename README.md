## Build

```
docker build -t webman .
```
## Usage

Start the Docker container:

### Linux

```
docker run --rm -it -p 8787:8787 -v /home/www/webman:/app webman
```

### Windows

```
docker run --rm -it -p 8787:8787 -v ./dev:/app webman
```

## Extensions

```
bash-5.1# php -m
[PHP Modules]
bcmath       
bz2
calendar     
Core
ctype        
curl
date
dom
event        
fileinfo     
filter       
ftp
gd
hash
iconv        
json
libxml       
mbstring     
mysqli       
mysqlnd      
openssl      
pcntl        
pcre
PDO
pdo_mysql    
pdo_sqlite   
Phar
posix        
readline     
redis        
Reflection   
session      
SimpleXML    
soap
sockets      
sodium       
SPL
sqlite3      
standard     
tokenizer
xml
xmlreader
xmlwriter
Zend OPcache
zip
zlib

[Zend Modules]
Zend OPcache
```
## Other 

delete all container
```
docker rm `docker ps -a -q`
```

delete all images
```
docker rmi -f $(docker images -qa)
```

## dos2unix install.sh

```
=> ERROR [ 7/14] RUN chmod +x install.sh     && sh install.sh     && rm -rf /tmp/extension                                                                 0.2s 
------
 > [ 7/14] RUN chmod +x install.sh     && sh install.sh     && rm -rf /tmp/extension:
: not foundll.sh: line 1: #!/bin/sh
: not foundll.sh: line 2:
: not foundll.sh: line 4:
: not foundll.sh: line 10: echo
: not foundll.sh: line 11:
: not foundll.sh: line 13:
: not foundll.sh: line 30:
0.217 install.sh: return: line 36: Illegal number: 0
```
查看文本格式
```
$ cat -A install.sh 
M-oM-;M-?#!/bin/sh^M$
^M$
```

> 执行转换
```
# 安装
sudo apt-get install dos2unix

# 转换
dos2unix install.sh
```
