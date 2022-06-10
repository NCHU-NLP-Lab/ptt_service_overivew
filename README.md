# Ptt_Service_Overivew

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

## 介紹PTT搜尋引擎的結構

### 結構圖

![PTT-dia2 drawio](https://user-images.githubusercontent.com/44884255/173089975-f33a99a9-f76e-4549-950c-655321ebc15c.png)

### 1. [前端+後端(Server)](https://github.com/NCHU-NLP-Lab/Ptt_SearchEngineWeb)
+ [Vue.js](https://vuejs.org/)
  + 漸進式 JavaScript 框架
  + 前端，網頁畫面，跟使用者互動
  + 在專案中負責 
    + 開發單頁應用程式
+ [Flask](https://flask.palletsprojects.com/en/2.0.x/)
  + 是一個使用 Python 撰寫的輕量級 Web 應用程式框架
  + 後端(Server)，接收前端的request
  + 在專案中負責 
    + 處理Request 
    + 對Elasticsearch下搜尋指令之API
### 2. [後端(Database)](https://github.com/NCHU-NLP-Lab/Ptt-Elasticsearch)
  + [elasticsearch](https://www.elastic.co/)
    + 是一個基於 Lucene 庫的搜尋引擎。它提供了一個分散式全文搜尋引擎，具有 HTTP Web 介面和無模式 JSON 文件，而 Elastic Cloud 是由 Elasticsearch 驅動的 SaaS 產品系列 
    + 在專案中負責
      + 建置於Kubernetes上 
      + 搜尋引擎
      + Database
  + [Kubernetes](https://kubernetes.io/)
    + 自動部署、擴充和管理「容器化（containerized）應用程式」的開源系統
    + 在專案中負責
      + 管理Container的運作
      + Workload balance
      
### 3. [爬蟲](https://github.com/NCHU-NLP-Lab/ptt-scrapy)
+ [python](https://www.python.org/)
  + 爬取熱門看版的文章 
  + 再以batch形式存於Data base

### 額外工具
+ [PTT monitor](https://github.com/NCHU-NLP-Lab/ptt-monitor)
  + LINE bot
  + 會根據觀察的ID，回傳該ID的留言紀錄
