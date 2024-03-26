---
title:  GuessTheNumber-UDP 
author: LiHsiang
date: 2022-01-16 2:00:00 +0800
categories: [Side Project,UDP]
tags: [Python,UDP,socket,threading]
# pin: true
image:
  path: /assets/img/UDP.png
  lqip: /assets/img/UDP.png
---
![GitHub last commit](https://img.shields.io/github/last-commit/Xiang511/GuessTheNumber-UDP?style=for-the-badge&color=%23007EC6){: .normal }
![Github Created At](https://img.shields.io/github/created-at/Xiang511/GuessTheNumber-UDP?style=for-the-badge&color=%23007EC6){: .normal }
![GitHub License](https://img.shields.io/github/license/XIang511/GuessTheNumber-UDP?style=for-the-badge&color=%23007EC6){: .normal }
<a href="https://github.com/Xiang511/GuessTheNumber-UDP">![Static Badge](https://img.shields.io/badge/Github-demo?style=for-the-badge&logo=github&color=%23000){: .normal }


創建一個UDP_SERVER玩猜數字遊戲 

最多可以三個人同時遊玩

## Features
- 最多可以三個人同時遊玩
- 採計時制，可以比賽看誰先解完

## Process introduction

- 首先用random產生一個答案
- 客戶端傳值(4個數字)
- Server判斷是否為正確格式
- 判斷輸入的數字 位置且數字也對回傳A 位置錯但數字對回傳B 
- 客戶端得到回覆(?A?B)
- 以此類推直到猜中正確答案
- 顯示花費多少時間

## Installation

>  Option 1. [GitHub Fork](https://github.com/Xiang511/GuessTheNumber-UDP)
{: .prompt-tip }
>  Option 2. [Download Zip](https://github.com/Xiang511/GuessTheNumber-UDP)
{: .prompt-tip }

## Usage

```console
Server-Example: python demo2.py server 0.0.0.0
```
```console
Client-Example: python demo2.py client 127.0.0.1 -p {port}
```
### Server
```python
def server(interface, port):
    th = []
    for i in range(3):
        server_sock.append(socket.socket(socket.AF_INET,socket.SOCK_DGRAM))
        server_sock[i].bind((interface,port+i))
        th.append(threading.Thread(target=server_action, args = (server_sock[i],i)))
    for i in range(3):
        th[i].start()
    for i in range(3):
        th[i].join()
```
### Server_Action
```python
def server_action(sock, number):
    time_start = time.time()
    print('Listening at', sock.getsockname())
    print(sum1)
    while True:
        data, address = sock.recvfrom(MAX_BYTES)  
        data = data.decode('ascii')
       
        print('Server {}:'.format(number)+'The client at {} says {!r}'.format(address, data))
        a = b = 0
        data = list(data)
        for i in range(4):
            if int(data[i]) in sum1:
                if int(data[i]) == sum1[i]:
                    a += 1
                else:
                    b += 1
            else:
                    continue
        if a != 4:
            data = str(a)+"A"+str(b)+"B"
        #print('Server {}:'.format(number)+'The client at {} says {!r}'.format(address, text))
        # message = '"{}"'.format(text)+'is {} bytes long'.format(len(data))
            message = data
            sock.sendto(message.encode('ascii'), address)
        else:
            message = " You are right!!!!!"
            time_end = time.time()    #結束計時
            time_c= time_end - time_start   #執行所花時間

            
            print('time cost', time_c, 's')
            print('Congratulations', sock.getsockname())
            
            sock.sendto(message.encode('ascii'), address)
            sum = random.sample(range(1, 10), 4) 
            
            break

```

### Client
```python
def client(hostname, port):
    sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
    sock.connect((hostname, port)) # 要先跟server建立連線，之後send資料不須指定地址
    print('Client socket name is {}'.format(sock.getsockname()))
    
    while True:
        text = input("Please enter the number >>>: ")
       
        if text == "|exit|":
            
            print(sock.getsockname(),'has leave the game')
            break

        if len(text) != 4:
            print("Wrong format,Please enter the correct format")
            continue
        if not text.isdecimal():
            print("Wrong format,Please enter the correct format")
            continue
        data = text.encode('ascii')
        sock.send(data) # sendto需指定接收ip，send不用(上面已經connect就可使用)

        data = sock.recv(MAX_BYTES)
        print('The server says {!r}'.format(data.decode('ascii')))
        if data.decode('ascii') == "You are right!!!!!":
            break
```



## Demo
![image](https://github.com/Xiang511/GuessTheNumber-UDP/assets/120042360/aa53a0f3-691a-454f-a549-71b2ff904ac7)
