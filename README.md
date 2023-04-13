# <p align="center">計畫進度報告</p>
<p align="right"><font size=2>第五組</font></p>

## 計畫主旨:	1. 使用癲癇患者腦波原始資料進行資料處理並分析，預測癲癇的發作

### 1.背景文獻的查詢情形
癲癇是一種常見的中樞神經系統慢性疾病，可以通過藥物治療來控制症狀。然而，對於某些患者，癲癇藥物可能無法完全控制症狀，或者可能產生嚴重的副作用。對於這些患者，手術治療可能是一個有效的選擇。手術治療通常是在停止藥物治療後對患者進行監測，以確定癲癇是否可以完全控制。在這段時間內，通常會進行頭皮腦電圖監測，以記錄癲癇發作的頻率和類型，以幫助醫生評估是否適合手術治療。[1]

而頑固型癲顯是指已經使用了兩種以上的藥物，且每種藥物都已經達到最大的合理治療劑量時，癲癇發作仍不能受到良好的控制，且發作頻率和嚴重程度都較高，目前治療方式多採用多種藥物組合，或者進行手術治療。目前決定的題目是分析患有頑固型癲癇的患者。

因此，目前決定的題目是分析患有頑固型癲癇的 22名受試者(分別為 5名年齡 3-22歲男性以及 17名年齡3-22歲女性)的腦電圖記錄（由波士頓兒童醫院兒科收集），並觀察受試者在停用抗癲癇藥物數天後，癲癇發作的情形以及狀態，並評估受試者是否適合進行手術治療。同時，我們也查詢了一些相關的訊號處理以及模型建立方法，利用小波轉換將腦波訊號處理以利後續作特徵提取以及深度學習模型。[2]

### 2.理論模式的建立情形
<img width="432" alt="圖片 1" src="https://user-images.githubusercontent.com/86188415/231790513-8f7d4b1a-c3dd-4be1-bc2c-1a8f29fb0330.png">
<ol>
<li>資料前處理：包括濾波、去噪、降采樣等。</li>
<li>Discrete	wavelet	transform：使用 Discrete	Wavelet	Transform	將 EEG 拆成五個部分，分別是：Delta	(1–4	Hz),	Theta	(4–8	Hz),	Alpha	(8–14	Hz),	Beta	(14–32	Hz),	and	Gamma	(32–64	Hz)[3]</li>
<li>特徵提取：包括時間領域、頻域和時頻域特徵的提取，例如振幅、功率、頻譜等。</li>
<li>分類器設計：可以選擇傳統的機器學習方法，如支持向量機（SVM）、隨機森林（RandomForest）、貝葉斯分類器等，也可以使用深度學習模型，如卷積神經網絡（CNN）、長短期記憶神經網絡（LSTM）等。</li>
<li>本次預計使用 CNN 模型來進行訓練。模型並不是本次重點，重點在於輸入資料的品質></li>
<li>模型評估：使用交叉驗證、ROC曲線、混淆矩陣等指標來評估模型的性能。</li>
</ol>

### 3.軟體程式的發展情形資料前處理使用 Matlab 來進行小波轉換、特徵提取和分類等模型建立與訓練使用 Python	3 在 Google	Colab 上進行
![圖片 1](https://user-images.githubusercontent.com/86188415/231790852-8f58ae8d-c768-4e9e-9fcd-12f2a50d6aca.png)
![圖片 1](https://user-images.githubusercontent.com/86188415/231790987-e28472a0-6cb5-4431-9185-6d404740a0ae.png)

### 4.預定進度表:(以甘氏圖為之，並以不同色筆區分目前工作進度)

![圖片 1](https://user-images.githubusercontent.com/86188415/231791923-08599fd6-87d9-43c5-acc3-06292c2c6389.png)

### 5.分工情形
<p>許家齊：軟體程式、數據資料處理、數據搜索、數據分析<p>
<p>江采彤：查找原始資料數據、文獻蒐集、甘氏圖美編、數據延伸應用<p>
<p>葉威廷：資料整理、數據探討、撰寫預期問題、程式撰寫<p>
<p>郭庭佑：模型評估、分析方法、蒐集資料、甘氏圖製作<p>

### 6.預期遭遇困難，及如何克服？
<ol>
<li>資料格式轉換問題：數據庫中的原始數據格式可能不適合用於某些分析工具，需要進行格式轉換。解決方法可以是使用專門的轉換工具，或者自行編寫轉換腳本。</li>
<li>資料品質問題：數據品質可能不夠理想，例如存在缺失值、雜訊等。解決方法可以是使用合適的數據清理技術，例如填充缺失值、濾除雜訊等。</li>
<li>資料分析問題：數據庫中的數據可能較為複雜，需要進行深入的數據分析才能獲得有意義的結果。解決方法可以是選擇合適的分析方法和工具，或者進行相關的數據挖掘和機器學習分析。</li>
<li>資料庫問題：使用者可能會遇到資料庫訪問問題，例如無法連接到資料庫，下載速度緩慢等。解決方法可以是檢查網絡連接，使用其他下載方式等。</li>
</ol>

### 7.參考資料(請以 EndNote 自動帶入文獻資料)
<ol>
<li>Ko, T.-S. and G.L. Holmes, EEG and clinical predictors of medically intractablechildhood epilepsy. Clinical Neurophysiology, 1999. 110(7): p. 1245-1251.</li>
<li>Shoeb, A.H., Application of machine learning to epileptic seizure onset detectionand treatment. 2009.</li>
<li>Shah, D., G. Gopan K., and N. Sinha, An investigation of the multi-dimensional (1Dvs. 2D vs. 3D) analyses of EEG signals using traditional methods and deeplearning-based methods. Frontiers in Signal Processing, 2022. 2.</li>
</ol>


