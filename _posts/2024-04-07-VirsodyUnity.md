---
title:  畢業專題 - Virsody 和 Unity 虛擬展間
author: LiHsiang
date: 2024-01-05 2:00:00 +0800
categories: [Graduation Project,Virsody & Unity虛擬展間]
tags: [Virsody,Unity,SketchFab,blender,C#]
# pin: true
image:
  path: /assets/img/AIC.png
  lqip: /assets/img/AIC.png
---
![GitHub last commit](https://img.shields.io/github/last-commit/Xiang511/Virsody-Unity?style=for-the-badge&color=blue){: .normal } 
![GitHub License](https://img.shields.io/github/license/Xiang511/Virsody-Unity?style=for-the-badge&color=blue){: .normal } 
<a href="https://github.com/Xiang511/Virsody-Unity/wiki/Virsody%E5%92%8CUnity%E8%99%9B%E6%93%AC%E5%B1%95%E9%96%93%E5%AF%A6%E4%BD%9C">![Static Badge](https://img.shields.io/badge/Wikipedia-Click%20to%20browse%20our%20wiki%20-Click%20to%20browse%20our%20wiki?style=for-the-badge&logo=wikipedia&color=blue){: .normal }





## 摘要

虛擬展間的概念類似googleMap，目的都是在不用出門的狀況下即可體驗風景或展覽。

與googleMap不同之處是，使用者可以和展間內的物品互動，同時使用者也可以在展間內自由走動觀賞作品，

展間視角為第一人稱大幅度的增加沉浸感。

## 一、簡介(研究動機&目的)
為了讓參訪者可以不用實際來到義守大學，也可以在手機或電腦上參觀科技5樓，我們製作了兩個虛擬參觀平台(網頁以及VR)。

參訪者只需在手機或電腦上開啟網頁或是使用VR下載我們的檔案，即可進入虛擬展間。

這個虛擬展間不僅省去了時間和距離的限制，還使參訪者能夠在舒適的環境中深入瞭解義守大學科技5樓的各個研究設備和成果。

我們期待這個創新的方式能夠為參訪者提供一個豐富而方便的參觀體驗。

未來，也將持續優化虛擬展間，讓參訪者可以獲得更加豐富的參觀體驗。

## 二、使用工具
主要使用: Virsody / Unity

輔助軟體/工具: Blender / Sketchfab

VR: Oculus-Quest2

使用語言: C#

## 三、預期成果
在虛擬展間中，參訪者可以自由地觀看場景和研究設備。

Virsody 平台還提供多媒體介紹(文字以及影片方式)，讓參訪者更全面地了解科技5樓的學術和研究成果。

Unity 平台則是使用VR來進行開發使用設備為Oculus的Quest2，透過VR的方式可以讓參訪者更加身臨其境地參觀科技5樓。

參訪者可以戴上 VR 頭盔，以 360 度的視角探索科技5樓的各個展區。參訪者可以透過頭部轉動和手部控制來移動視角。

## 四、實施流程
1.	按照五樓平面設計圖，量測需要的尺寸以及預估場景規模。
2.	在Unity和Virsody內，構建場景基本雛形以及規劃空間。
3.	利用Blender做出專題機器模型。
4.	把做好的物件，匯入至Unity和Virsody裡面，並加以排列整理。
5.	打磨場景細節。
6.	VR部分使用C#語言編寫script來實現移動和視角轉動

[Blender物件製作過程](https://github.com/Xiang511/Virsody-Unity/wiki/Sketchfab%E6%87%89%E7%94%A8%E8%88%87Blender%E7%89%A9%E4%BB%B6%E8%A3%BD%E4%BD%9C)

[Virsody專案建置過程](https://github.com/Xiang511/Virsody-Unity/wiki/Virsody%E5%B0%88%E6%A1%88%E5%BB%BA%E7%BD%AE%E9%81%8E%E7%A8%8B)

[Unity專案建置過程](https://github.com/Xiang511/Virsody-Unity/wiki/Unity%E5%B0%88%E6%A1%88%E5%BB%BA%E7%BD%AE%E9%81%8E%E7%A8%8B)

## 五、成果與結論

虛擬展間在近年來逐漸受到重視，並已在各領域應用。

藝術館可以用虛擬展間舉辦線上展覽，讓觀眾不必親臨現場也能欣賞藝術作品。

企業可以利用虛擬展間舉辦線上產品發表會，讓客戶深入地了解產品。

[Virsody線上展間](https://virsody.io/r/isu10903070)

[UnityVR展間-Demo](https://www.youtube.com/watch?v=eMP0fmyXkTM)


## 六、參考資料
[1]	 C#教學: [https://unity.com/how-to/learning-c-sharp-unity-beginners](https://unity.com/how-to/learning-c-sharp-unity-beginners)

[2]	 VR教學: [https://learn.unity.com/](https://learn.unity.com/)

[3]	 Virsody手冊: [https://hei-dong-chuang-zao.gitbook.io/virsody-guide/](https://hei-dong-chuang-zao.gitbook.io/virsody-guide/)

[4]	 Blender手冊: [https://docs.blender.org/manual/zh-hant/2.81/about/introduction.html](https://docs.blender.org/manual/zh-hant/2.81/about/introduction.html)

[5]	Sketchfab Blog : [https://sketchfab.com/blogs/community?ref=header](https://sketchfab.com/blogs/community?ref=header)

[6]	Oculus Quest2: [https://www. meta.com/tw/quest/products/quest-2/](https://www.%20meta.com/tw/quest/products/quest-2/)