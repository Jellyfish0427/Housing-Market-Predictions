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
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/assets/128220508/fd881209-f036-42d7-a935-10375a0bab31)  

#### (2) 主要建材
mapping: 鋼筋混凝土造:1, 鋼骨造:2, 加強磚造:3, 其他:0
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/assets/128220508/0a456166-c766-465a-ba1e-7a9e1c28b14e)

#### (3) 建物型態
mapping: 住宅大樓:1, 公寓 3:華廈 4:透天厝 其他:0
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/assets/128220508/1026becc-a79c-4cc6-885c-931ccdcc4404)

#### (4) 主要用途 
mapping: 住家用:1, 集合住宅:2, 商業用:3, 一般事務所:4, 國民住宅:5, 住商用:6, 工業用:7, 辦公室:8, 住工用:9, 店鋪:10, 廠房:11, 其他:0
![image](https://github.com/Jellyfish0427/Housing-Market-Predictions/assets/128220508/cb82c84e-516d-4d23-99be-20a8ff42de84)

#### (5) 縣市
mapping: 基隆市:1, 台北市:2, 新北市:3, 桃園市:4, 新竹市:5, 新竹縣:6, 苗栗縣:7, 台中市:8, 彰化縣:9, 南投縣:10, 雲林縣:11, 嘉義市:12, 嘉義縣:13, 台南市:14, 高雄市:15, 屏東縣:16, 台東縣:17, 花蓮縣:18, 宜蘭縣:19, 澎湖縣:20, 金門縣: 21, 連江縣:22













