# ptt_service_overivew

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

## 介紹PTT搜尋引擎的結構

### 結構圖

![ptt_structure](https://user-images.githubusercontent.com/44884255/154961477-7120b710-af9d-4501-8654-15e38290e029.png)

## PTT搜尋引擎的結構可以分為
1. 前端 --- https://github.com/NCHU-NLP-Lab/Ptt_SearchEngineWeb
2. 後端 --- https://github.com/NCHU-NLP-Lab/Ptt-Elasticsearch
3. 爬蟲 --- https://github.com/NCHU-NLP-Lab/ptt-scrapy

### 1. 前端 
+ Vue.js
  + 開發單頁應用程式
+ Flask
  + 處理Request
  + 對Elasticsearch下搜尋指令之API

### 2. 後端
+ Elasticsearch
  + 管理Container運作
  + Workload balance
+ elasticsearch
  + 搜尋引擎
  + Database
### 3. 爬蟲
+ python
  + 爬取熱門看版的文章 
  + 再以batch形式存於Data base

### 額外工具
+ PTT monitor --- https://github.com/NCHU-NLP-Lab/ptt-monitor
  + LINE bot
  + 會根據觀察的ID，回傳該ID的留言紀錄
