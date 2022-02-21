# ptt_service_overivew

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

## 介紹PTT搜尋引擎的結構

### 結構圖

![ptt_structure](https://user-images.githubusercontent.com/44884255/154961477-7120b710-af9d-4501-8654-15e38290e029.png)

### 1. [前端](https://github.com/NCHU-NLP-Lab/Ptt_SearchEngineWeb)
+ [Vue.js](https://vuejs.org/)
  + 漸進式 JavaScript 框架
  + 在專案中負責 
    + 開發單頁應用程式
+ [Flask](https://flask.palletsprojects.com/en/2.0.x/)
  + 是一個使用 Python 撰寫的輕量級 Web 應用程式框架
  + 在專案中負責 
    + 處理Request 
    + 對Elasticsearch下搜尋指令之API

### 2. [後端](https://github.com/NCHU-NLP-Lab/Ptt-Elasticsearch)
+ [Kubernetes](https://kubernetes.io/)
  + 自動部署、擴充和管理「容器化（containerized）應用程式」的開源系統
  + 在專案中負責
    + 管理Container的運作
    + Workload balance
+ [elasticsearch](https://www.elastic.co/)
  + 是一個基於 Lucene 庫的搜尋引擎。它提供了一個分散式全文搜尋引擎，具有 HTTP Web 介面和無模式 JSON 文件，而 Elastic Cloud 是由 Elasticsearch 驅動的 SaaS 產品系列 
  + 在專案中負責
    + 搜尋引擎
    + Database
### 3. [爬蟲](https://github.com/NCHU-NLP-Lab/ptt-scrapy)
+ [python](https://www.python.org/)
  + 爬取熱門看版的文章 
  + 再以batch形式存於Data base

### 額外工具
+ [PTT monitor](https://github.com/NCHU-NLP-Lab/ptt-monitor)
  + LINE bot
  + 會根據觀察的ID，回傳該ID的留言紀錄
