# Housing Market Predictions
## Data Process
### 1. Delete Outliers
- 土地面積：刪除 >7.12 和 <-1.65 的資料
- 移轉層數：刪除 >35 的資料
- 總樓層數：刪除 >41 的資料
- 建物面積：刪除 >6.02 和 <-1.8 的資料
- 車位面積：刪除 >5.15 和 <-0.82 的資料
- 主建物面積：刪除 >5.85 和 <-2.03 的資料
- 陽台面積：刪除 >4.9 和 <-1.65 的資料
- 附屬建物面積：刪除>13.31和 <-0.44 的資料

### 2. Use external data to increase features
- 計算最近的火車站	以及 與最近火車站的距離  
- 方圓800公尺內捷運站數量  
- 方圓300公尺內便利商店數量 	  
- 方圓300公尺內國小數量    
- 方圓800公尺內國中數量    
- 方圓1000公尺內高中數量	   
- 方圓1000公尺內大學數量    
- 方圓1000公尺內金融機構數量   
- 方圓300公尺內醫院數量   

### 3. Mapping features
#### (1) 使用分區
mapping: 住:1, 商:2, 農:3, 工:4, 其他:0
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/使用分區.png)  

#### (2) 主要建材
mapping: 鋼筋混凝土造:1, 鋼骨造:2, 加強磚造:3, 其他:0
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/主要建材.png)

#### (3) 建物型態
mapping: 住宅大樓:1, 公寓 3:華廈 4:透天厝 其他:0
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/建物型態.png)

#### (4) 主要用途 
mapping: 住家用:1, 集合住宅:2, 商業用:3, 一般事務所:4, 國民住宅:5, 住商用:6, 工業用:7, 辦公室:8, 住工用:9, 店鋪:10, 廠房:11, 其他:0
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/主要用途.png)

#### (5) 縣市
mapping: 基隆市:1, 台北市:2, 新北市:3, 桃園市:4, 新竹市:5, 新竹縣:6, 苗栗縣:7, 台中市:8, 彰化縣:9, 南投縣:10, 雲林縣:11, 嘉義市:12, 嘉義縣:13, 台南市:14, 高雄市:15, 屏東縣:16, 台東縣:17, 花蓮縣:18, 宜蘭縣:19, 澎湖縣:20, 金門縣: 21, 連江縣:22  
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/縣市.png)  
從上圖可以看到六都的資料數量特別多，因此針對六都的鄉鎮市區建立新的feature並進行mapping

**(a) 台北市**  
mapping: 大安區: 1, 中山區: 2, 內湖區: 3, 信義區: 4, 士林區: 5, 文山區: 6, 松山區: 7, 北投區: 8, 中正區: 9, 萬華區: 10, 大同區: 11, 南港區: 12, 其他: 0, 別的縣市: -1  
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/台北市-鄉鎮市區.png)  

**(b) 新北市**  
mapping: 板橋區:1, 新莊區:2, 中和區:3, 三重區:4, 汐止區:5, 新店區:6, 土城區:7, 林口區:8, 永和區:9, 淡水區:10, 蘆洲區:11, 五股區:12, 樹林區:13, 三峽區:14, 鶯歌區:15, 泰山區:16, 深坑區:17, 八里區:18, 其他: 0, 別的縣市: -1  
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/新北市-鄉鎮市區.png)

**(c) 桃園市**  
mapping: 桃園區:1, 中壢區:2, 蘆竹區:3, 八德區:4, 龜山區:5, 平鎮區:6, 楊梅區:7, 大園區:8, 大溪區:9, 龍潭區:10, 觀音區:11, 其他: 0, 別的縣市: -1   
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/桃園市-鄉鎮市區.png)

**(d) 台中市**  
mapping: 西屯區:1, 北屯區:2, 南屯區:3, 南區:4, 西區:5, 北區:6, 太平區:7, 大里區:8, 潭子區:9, 烏日區:10, 東區:11, 豐原區:12, 神岡區:13, 大雅區:14, 中區:15, 其他: 0, 別的縣市: -1   
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/台中市-鄉鎮市區.png)

**(e) 台南市**  
mapping: 永康區:1, 安平區:2, 北區:3, 東區:4, 中西區:5, 南區:6, 安南區:7, 仁德區:8, 善化區:9, 新市區:10, 新營區:11, 其他: 0, 別的縣市: -1   
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/台南市-鄉鎮市區.png)

**(f) 高雄市**  
mapping: 鼓山區:1, 三民區:2, 左營區:3, 楠梓區:4, 鳳山區:5, 苓雅區:6, 前鎮區:7, 前金區:8, 新興區:9, 仁武區:10, 小港區:11, 橋頭區:12, 鹽埕區:13, 岡山區:14, 鳥松區:15, 其他: 0, 別的縣市: -1   
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/高雄市-鄉鎮市區.png)

### 4. New Features
- 用 建物面積/土地面積 建立 **建物佔地比**
- 用 移轉層次/總樓層數 建立 **樓高比**

### 5. Dropoff 
- ID
- 鄉鎮市區
- 路名
- 備註

## Model
XGBoost

## Result
Private score: 8.6447709  
Rank: #109 (972 teams in total)

This comprehensive approach to data processing, feature engineering, and modeling contributed to achieving a competitive ranking in the competition.




