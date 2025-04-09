# Shallow Machine Learning Project

本專案包含了幾個基於淺層機器學習的實驗，用於探索不同的機器學習模型和各種資料集。淺層機器學習模型主要指的是使用較少層數的模型進行學習的技術，與深度學習（Deep Learning）相比，通常具有較少的參數，計算需求較低一些，但仍能夠解決各種實際問題。這個專案旨在展示這些技術如何在各種資料集上進行應用和效果評估。

專案中使用了多種資料集，包括手寫數字、人臉影像辨識等，並涵蓋了不同的算法和模型，如主成分分析（PCA）、奇異值分解（SVD）、支持向量機（SVM）、卷積神經網路（CNN）等，對它們進行了詳細的分析和比較。
## :open_file_folder: 資料夾結構

:pushpin: **HTML**: 相關大型實驗的 HTML 輸出文件，這些文件包含了實驗結果的詳細展示
  - `SML_3_ClassifierExp_AT&T.html`: AT&T 人臉資料集分類實驗結果
  - `SML_3_ClassifierExp_YaleFaces.html`: Yale Faces 資料集分類實驗結果
  - `SML_3_ClassifierExp_wine.html`: Wine 資料集分類實驗結果
  - `SML_4_CNN&YaleFace.html`: 卷積神經網路與 Yale Faces 資料集分類實驗結果

:pushpin: **Pretrain.file**: 內含預訓練模型檔案
  - `YaleFaces_net.pt`: 預訓練的 Yale Faces 模型
  - `digit10_net.pt`: 預訓練的 digit10 模型

:pushpin: **ipynb**: 主要實作的 Jupyter Notebook 文件，展示了不同的機器學習實驗過程
  - `SML_1_PCA.ipynb`: 主成分分析（PCA）實驗
  - `SML_2_SVD&ImageFeatures.ipynb`: 奇異值分解（SVD）與影像特徵提取實驗
  - `SML_3_ClassifierExp_AT&T.ipynb`: AT&T 人臉資料集分類器實驗
  - `SML_3_ClassifierExp_YaleFaces.ipynb`: Yale Faces 資料集分類器實驗
  - `SML_3_ClassifierExp_wine.ipynb`: Wine 資料集分類器實驗
  - `SML_4_CNN&YaleFace.ipynb`: 卷積神經網路與 Yale Faces 資料集分類器實驗
  - `SML_4_mnist_tensorflow_torch.ipynb`: 使用 TensorFlow 和 PyTorch 進行手寫數字識別（MNIST）實驗

## :books: 詳細介紹

### ipynb 資料夾中的檔案：

### :one: **SML_1_PCA.ipynb**

包含了兩個主成分分析（PCA）實驗，目標是探索資料中的結構和模式。

1. 紅酒資料集分析：透過主成分分析，探索義大利某地區三個紅酒製造商生產的178支紅酒中13種化學成分之間的關係。將高維資料降至二維和三維空間，並進行資料可視化，以揭示紅酒樣本中的結構模式。

2. 乳癌腫瘤影像分析：對乳癌患者的腫瘤影像量測資料進行PCA，目的是發現不同量測變數中的主要模式和變異，進而評估這些特徵對於區分惡性與良性腫瘤的重要性，幫助進一步理解腫瘤特徵。

<hr>

### :two: **SML_2_SVD&ImageFeatures.ipynb**:

包含四個關於圖像處理和特徵提取的實驗。

1. 圖像壓縮與區域比較：比較不同大小的小區域（patch）對圖像壓縮效果的影響，並觀察在相同壓縮比率下，不同重組方式對還原後圖像品質的影響。

2. 圖像加密與解密：利用 SVD 分解對灰度圖像進行加密，並根據不同奇異值數量觀察加密和解密過程中圖像品質的變化，並進行不同圖像的加密實驗。

3. 手寫數字數據集展示：加載並隨機展示手寫數字圖像，檢視資料型態及影像內容。

4. 手寫數字圖像壓縮：使用 SVD 對手寫數字圖像進行壓縮，並根據不同壓縮比率比較原始圖像與壓縮後還原圖像的差異。

<hr>

### :dart: SML_3 目標：

使用標準化資料與主成分資料進行訓練，並比較三種分類器在不同資料上的準確率表現
- Logistic Regression
- Support Vector Machine
- Neural Network

###  :three: **SML_3_ClassifierExp_AT&T.ipynb**:

:bar_chart: 觀察結果：

- 在 AT&T 的人臉資料中，無論是標準化資料還是主成分資料，Logistic Regression 都取得了最佳的分類準確率。

- 其中，使用主成分資料訓練的模型在 Logistic Regression 和 Neural Network 中的表現優於使用原始資料。主成分分析有助於去除噪聲，將資料轉換成更具代表性的特徵空間，提升了模型效能。



###  :four: **SML_3_ClassifierExp_YaleFaces.ipynb**:
- 對於耶魯人臉資料來說，在標準化原始資料中，三種分類器的最高準確率均相近，其中 SVM 和 Neural Network 的準確率達到 94.74%，為最高。

- 在主成分資料中，分類準確率存在顯著差異，SVM 的準確率最高，達到 83.96%。

- 總體來看，標準化原始資料表現穩定，準確率接近，而主成分資料則對分類器的表現有更大的影響，SVM 在此資料集上表現最佳。

###  :five: **SML_3_ClassifierExp_wine.ipynb**:
- 在葡萄酒資料中，原始資料的分類準確率最高可達 96.3%，無論分類器為何。

- 在主成分資料中，所有分類器的準確率均為 96.3%。這顯示選取足夠的主成分後，已經包含了原始資料的大部分信息。

- 由於資料集較小且選取的主成分涵蓋了大部分舊資訊，三種分類器的結果差異極小，表現幾乎相同。

<hr>

###  :six: **SML_4_CNN&YaleFace.ipynb**:

:bar_chart: 目標：

展示如何使用卷積神經網路（CNN）對耶魯人臉資料進行預測，並介紹如何將資料轉換為適用於 PyTorch 的格式，設定卷積神經網路各層，進行訓練與預測。

:paperclip: 內容：

- 資料準備：
將 NumPy 陣列轉換為 Tensor 型態，使用 .float() 和 .long() 確保資料類型適合訓練與測試。

- 卷積神經網路（CNN）設計：設定四層卷積層，包含批次歸一化層和 ReLU 激活函數；全連接層用於將卷積層提取的特徵映射到最終的分類結果。

- 前向傳播：
資料依次經過卷積層、批次歸一化層、最大池化層、全連接層等，最終輸出分類結果。

- 儲存模型：
將訓練好的模型儲存為 .pt 檔案，用於後續預測。

- 預測與評估：
展示神經網路在測試資料上的預測結果，並計算準確率。

最後，讀取已訓練模型進行預測，並觀察是否能正確分類耶魯人臉圖像。

<hr>

###  :seven: **SML_4_mnist_tensorflow_torch.ipynb**:
  - 使用 TensorFlow 和 PyTorch 框架來實現手寫數字識別（MNIST）任務，並比較兩種深度學習框架
