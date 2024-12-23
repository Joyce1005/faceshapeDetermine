# 能「顏」善「辨」——臉型智能診斷與推薦系統

這是一個基於 Flask 框架開發的臉型辨識網站。使用者可以選擇上傳照片或直接拍照，系統會辨識臉型並推薦適合的髮型與配飾，提升個人造型搭配的便利性。

---

## 📋 功能特色

- **臉型辨識**：根據使用者上傳的照片，辨識出6種類型的臉型（長臉、方臉、圓臉、鵝蛋臉、菱形臉、心型臉）。
- **髮型推薦**：依據臉型建議多款適合的髮型。
- **配飾建議**：推薦符合臉型的眼鏡、耳環等配飾。
- **用戶調整**：若偵測結果不符，使用者可以手動微調特徵點位置。

---

## 🛠️ 環境需求

- **Python**：版本 3.8 或以上
- **相關套件**：
  - Flask
  - OpenCV
  - OpenFace
  - Bootstrap (前端框架)

---

## 🚀 安裝與執行


### 1. 下載專案
將專案放置於桌面(C:\Users\user\Desktop\Flask)，或是更改faceshapeDetermine.py中rootPath路徑

### 2. 建立環境
python -m venv venv
source venv/bin/activate   # Linux / macOS
venv\Scripts\activate      # Windows

### 3. 安裝依賴
pip install -r requirements.txt

### 4. 安裝openssl
https://slproweb.com/products/Win32OpenSSL.html

### 5. 設置openssl(第一次安裝或遇到IP變動時)
1. 打開openssl.cnf
2. CN = 192.168.0.142 改成主機IP
3. IP.1 = 192.168.0.142 改成主機IP
4. 打開CMD，切換到(cd) C:\Users\user\Desktop\Flask
5. 輸入
openssl genpkey -algorithm RSA -out server.key -aes256
openssl req -new -key server.key -out server.csr -config openssl.cnf
openssl x509 -req -days 365 -in server.csr -signkey server.key -out server.crt -extensions req_ext -extfile openssl.cnf


### 4. 執行網站
1. python faceshapeDetermine.py
2. 輸入三次openssl設置的密碼
3. 在瀏覽器中開啟 https://IP位置:5443


