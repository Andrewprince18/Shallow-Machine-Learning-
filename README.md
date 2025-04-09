# Shallow Machine Learning Project

這個專案包含了幾個基於淺層學習（Shallow Learning）的實驗，包含了不同的機器學習模型和資料集。該專案包括以下資料夾和文件：

## 資料夾結構

- **HTML**: 相關大型實驗的 HTML 輸出文件，這些文件包含了實驗結果的詳細展示
  - `SML_3_ClassifierExp_AT&T.html`: AT&T 人臉資料集分類實驗結果
  - `SML_3_ClassifierExp_YaleFaces.html`: Yale Faces 資料集分類實驗結果
  - `SML_3_ClassifierExp_wine.html`: Wine 資料集分類實驗結果
  - `SML_4_CNN&YaleFace.html`: 卷積神經網路與 Yale Faces 資料集分類實驗結果

- **Pretrain.file**: 內含預訓練模型檔案
  - `YaleFaces_net.pt`: 預訓練的 Yale Faces 模型
  - `digit10_net.pt`: 預訓練的 digit10 模型

- **ipynb**: 主要實作的 Jupyter Notebook 文件，展示了不同的機器學習實驗過程
  - `SML_1_PCA.ipynb`: 主成分分析（PCA）實驗
  - `SML_2_SVD&ImageFeatures.ipynb`: 奇異值分解（SVD）與影像特徵提取實驗
  - `SML_3_ClassifierExp_AT&T.ipynb`: AT&T 人臉資料集分類器實驗
  - `SML_3_ClassifierExp_YaleFaces.ipynb`: Yale Faces 資料集分類器實驗
  - `SML_3_ClassifierExp_wine.ipynb`: Wine 資料集分類器實驗
  - `SML_4_CNN&YaleFace.ipynb`: 卷積神經網路與 Yale Faces 資料集分類器實驗
  - `SML_4_mnist_tensorflow_torch.ipynb`: 使用 TensorFlow 和 PyTorch 進行手寫數字識別（MNIST）實驗

## 主要介紹

### ipynb 資料夾中的檔案：

- **SML_1_PCA.ipynb**:
  - 進行主成分分析（PCA），用於資料降維，並分析其在機器學習模型中的應用
  
- **SML_2_SVD&ImageFeatures.ipynb**:
  - 進行奇異值分解（SVD）以提取影像特徵，並展示其在影像處理中的應用

- **SML_3_ClassifierExp_AT&T.ipynb**:
  - 使用 AT&T 人臉資料集進行分類實驗，展示了如何使用基本的機器學習模型進行影像分類

- **SML_3_ClassifierExp_YaleFaces.ipynb**:
  - 使用 Yale Faces 資料集進行人臉辨識分類實驗

- **SML_3_ClassifierExp_wine.ipynb**:
  - 使用 Wine 資料集進行多類別分類實驗，展示不同機器學習算法的效果

- **SML_4_CNN&YaleFace.ipynb**:
  - 使用卷積神經網路（CNN）對 Yale Faces 資料集進行分類，展示深度學習模型的應用

- **SML_4_mnist_tensorflow_torch.ipynb**:
  - 使用 TensorFlow 和 PyTorch 框架來實現手寫數字識別（MNIST）任務，並比較兩種深度學習框架
