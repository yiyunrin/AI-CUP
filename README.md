# AI CUP

## 檔案介紹

### 資料前處理
資料前處理有以下4個程式碼：
1. data preprocessing_kyu_dan.ipynb：<br/>
用來處理kyu和dan的training dataset，將資料轉換成hdf5檔。
2. data preprocessing_style_best.ipynb：<br/>
用來處理play style的training dataset，將資料轉換成hdf5檔。
3. data preprocessing_test_dan_kyu.ipynb：<br/>
用來處理kyu和dan的public test和private test的資料，將資料轉換成hdf5檔。
4. data preprocessing_test_style.ipynb：<br/>
用來處理play style的public test和private test的資料，將資料轉換成hdf5檔。
    
### Training
訓練模型有以下3個程式碼，分別用來訓練Dan, Kyu, PlayStyle的模型：
1. Dan Training.ipynb
2. Kyu Training.ipynb
3. PlayStyle Training.ipynb

### 預測和寫檔
1. Create Upload CSV.ipynb：<br/>用來預測結果和寫要上傳到AI CUP上的CSV檔。

## 使用說明

### 環境
- CUDA 11.2
- cuDNN 8.1
### 函式庫
- TensorFlow 2.9.1
- h5py 3.10.0
- numpy 1.24.4
### 使用方法
一、 將training dataset的csv檔轉成hdf5檔
- 執行"data preprocessing_kyu_dan.ipynb"來處理kyu和dan的訓練資料
    - 輸入：dan和kyu訓練資料的csv檔。
    - 輸出：dan和kyu訓練資料的兩個hdf5檔。
- 執行"data preprocessing_style.ipynb"來處理play style的訓練資料
    - 輸入：play style訓練資料的csv檔。
    - 輸出：play style訓練資料的hdf5檔。
    
二、 開始訓練模型
- 執行"Dan Training.ipynb"
    - 輸入：dan訓練資料的hdf5檔。
    - 輸出：dan的模型。
- 執行"Kyu Training.ipynb"
    - 輸入：kyu訓練資料的hdf5檔。
    - 輸出：kyu的模型。
- 執行"PlayStyle Training.ipynb"
    - 輸入：play style訓練資料的hdf5檔。
    - 輸出：play style的模型。
    
三、 將要預測的dataset的csv檔轉成hdf5檔
- 執行"data preprocessing_test_dan_kyu.ipynb"來處理kyu和dan的預測資料
    - 輸入：dan和kyu預測資料的csv檔。
    - 輸出：dan和kyu預測資料的hdf5檔。
- 執行"data preprocessing_test_style.ipynb"來處理play style的預測資料
    - 輸入：play style預測資料的csv檔。
    - 輸出：play style預測資料的hdf5檔。
    
四、預測並寫檔
- 執行"Create Upload CSV.ipynb"
    - 輸入：
        1. dan, kyu, play style預測資料的hdf5檔。
        2. dan, kyu, play style的模型。
    - 輸出：預測結果的csv檔。
