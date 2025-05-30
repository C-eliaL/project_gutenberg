

# Project Gutenberg 中文書籍爬蟲

共爬取 227 本書籍（找到 507 本書的連結，於下載滿 200 以上後，手動停止執行）

## 安裝套件

    requests                2.32.3
    beautifulsoup4          4.13.4

## 專案結構

```
ProjectGutenberg/
├── README.md
├── gutenberg.ipynb
├── project_gutenberg/ （爬取到的 .txt 中文書籍將儲存在此資料夾）
```

## 功能流程

1. 下載 requests, bs4, os, pprint, re 套件
2. 指定連結，建立資料夾
3. 建立 .txt 檔

### 模組細節

* **A. 抓取書籍連結總數**：計算可下載書籍數
* **B. 建立爬取中文的正規表達式**：過濾非中文資料
* **C. 建立迴圈**：依序下載書名及其連結內容

  * 下載書籍連結的內文將內文寫進新檔 .txt 檔

### 錯誤處理

1. 程式會自動過濾獲取的書名中包含的非法字元（如 `/ \ : * ? " < > | \r \n`），確保生成的檔案名稱是合法的。
2. 下載連結檢查：若某本書籍無法找到其 `.txt.utf-8` 下載連結，程式會自動跳過該書並印出提示訊息，繼續處理下一本書籍。

## 成果影片連結

[點我觀看](https://drive.google.com/file/d/1THbZ4ekJA5E0GLtxnK1HXSn-N2SZX63b/view?usp=sharing)


