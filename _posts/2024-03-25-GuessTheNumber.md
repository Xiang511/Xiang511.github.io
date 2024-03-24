---
title:  GuessTheNumber-UDP 
author: LiHsiang
date: 2022-1-16 2:00:00 +0800
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


1A2B-猜數字

創建一個UDP_SERVER玩猜數字遊戲

最多可以三個人同時遊玩

採計時制，可以比賽看誰先解完

## 流程介紹

1.首先用random產生一個答案

2.客戶端傳值(4個數字)

3.Server判斷是否為正確格式

4.判斷輸入的數字 位置且數字也對回傳A 位置錯但數字對回傳B 

5.客戶端得到回覆(?A?B)

6.以此類推直到猜中正確答案

7.顯示花費多少時間

## 主要判斷式
```python
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
```

## Demo
![image](https://github.com/Xiang511/GuessTheNumber-UDP/assets/120042360/aa53a0f3-691a-454f-a549-71b2ff904ac7)
