---
title:  Teacher Query System 
author: LiHsiang
date: 2023-01-10 2:00:00 +0800
categories: [Side Project,Website]
tags: [HTML,CSS,Javascript,Jquery,JSP,Java,BootStrap5,Apache TomCat,Microsoft SQL Server]
# pin: true
image:
  path: /assets/img/TeacherQuerySystem.png
  lqip: /assets/img/TeacherQuerySystem.png
---
![GitHub last commit](https://img.shields.io/github/last-commit/Xiang511/TeacherQuerySystem?style=for-the-badge&color=%23007396){: .normal }
![Github Created At](https://img.shields.io/github/created-at/Xiang511/TeacherQuerySystem?style=for-the-badge&color=%23007396){: .normal }
![GitHub License](https://img.shields.io/github/license/XIang511/TeacherQuerySystem?style=for-the-badge&color=%23007396){: .normal }
<a href="https://youtu.be/BjJkCcQfMJY">![Static Badge](https://img.shields.io/badge/Demo-YouTube-YouTube?style=for-the-badge&logo=youtube&color=red){: .normal }


利用 Microsoft SQL Server, Java Server Pages , Bootstrap5 , Jquery ,apache-tomcat

實現一個教師資料查詢系統，主要使用 ODBC 連線，[點擊前往](https://github.com/Xiang511/TeacherQuerySystem).

## Features

- 教師資料
   新增 刪除 修改 查詢
- 專長資料
  新增 刪除 修改 查詢
- 系級名稱
  修改 查詢


## Usage
請忽略 "網站" 資料夾內的檔案，請使用demo2壓縮檔
> ### 前置步驟
> 下載 Miscrosoft SQL Server<br>
> 下載 SSMS<br>
> 下載 jdk-8u131-windows-x64.exe<br>
> 下載 java-ide ex: <a href="https://www.eclipse.org/downloads/">eclipse</a> (本專案使用 neon3 版本)<br>
> 下載 apache (本專案使用 8.5.14) 檔案位於列表中<br><br>
{: .prompt-info }

### Eclipse 設定
---

#### eclipse 創建一個 dynamic web project ，下圖名稱為test

#### 配置 apache jdk 於 eclipse

#### 將 demo2\demo2\WebContent\資料庫期末\110-1_Orders 匯入專案(匯入110-1_Orders即可)

#### lib與JavaResources配置參照下圖

 - lib demo2\demo2\WebContent\WEB-INF\lib (直接複製檔案即可)

![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/8f1ba456-4041-4893-b2a4-6b7cff53147d){: .normal }

 - JavaResources demo2\demo2\build\classes
![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/908086f6-d70b-4fec-bbb3-4d7eb619dc50){: .normal }


#### 完整配置圖
---

![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/a13e572b-7522-4c74-8f62-a23a71d3e82d){: .normal }

### Miscrosoft SQL Server 設定
---

#### 在mssql中新建一個資料庫，創建檔案位於列表中 (亦可使用掛載資料庫方式)

#### 在 mssql設定管理員中 中開啟 TCP port 1443 , 並將服務重新啟動

![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/aebf14ae-b66d-4dc3-a3dd-d8c3d91fbb8a){: .normal }{: width="500" height="400" }
![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/43f9e1c4-4325-48af-a0be-725d57e0122c){: .normal }{: width="500" height="400" }
  
#### 在ssms中 新增使用者demo，密碼demo ，使用sql驗證登入
---


![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/2307f0cb-4aea-4ad9-b8a3-8940a1f3d83c){: .normal }{: width="500" height="400" }
![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/34b8e7eb-8eb5-4447-b56c-d59246967ba9){: .normal }{: width="500" height="400" }
![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/ba8ce5bc-a6ba-4e58-a292-6c44272d686b){: .normal }{: width="500" height="400" }

## Demo
---

{% include embed/youtube.html id='BjJkCcQfMJY?si=JtM80u-UnLlk0GIf' %}




## 無法連線問題
---
Q:使用者無法登入

![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/e9bfb730-c738-4b87-bf3a-546bc2319abe)

A:可能未開啟sql驗證登入

Q:路徑問題

![image](https://github.com/Xiang511/TeacherQuerySystem/assets/120042360/e8766a15-80bb-4361-968c-5aabf79ef9af)

A:修改即可
