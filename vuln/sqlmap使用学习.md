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

- 判断是否存在get请求sql注入
  ```sh
  sqlmap.py -u “http://192.168.1.1/get_int.php？id=xxx" 
  ```

- 判断是否存在post请求方式注入

  - 将post请求包保存到文本中

  ```sh
  sqlmap.py -r " 路径" 
  --dbs  //数据库
  --current-db //当前数据库
  --tables //表名
  --columns //行
  --dump 
  ```

  