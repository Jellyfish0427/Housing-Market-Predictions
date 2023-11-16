# Housing-Market-Predictions
## Competition: 
https://tbrain.trendmicro.com.tw/Competitions/Details/30  

## Dataset
### Features
<img src="https://github.com/Jellyfish0427/Housing-Market-Predictions/blob/main/image/features.png" alt="image" width="500">

### External data
- 大學基本資料.csv
- 高中基本資料.csv
- 國中基本資料.csv
- 國小基本資料.csv
- 火車站點資料.csv
- 捷運站點資料.csv
- 金融機構基本資料.csv
- 便利商店.csv
- 醫療機構基本資料.csv


## Evaluate
Using **MAPE** (Mean Absolute Percentage Error) to evaluate model performance.  

$$
MAPE = \frac{1}{N} \sum_{i=1}^{N} \left| \frac{y_i - \hat{y}_i }{y_i} \right| \times 100\%  
$$  

where N is the total number of data, yi is the true price, and ^yi represents the predicted price.
