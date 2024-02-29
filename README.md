# Golf-Ball-Trajectory-Estimation
시계열 데이터 기반 골프공 궤적 예측 모델 개발 프로젝트🏌️‍♂️

## 기술 스택


## 🧑‍💻 Manual

[Train Manual](https://rogue-impatiens-fb5.notion.site/Train-Manual-a205e357d37e42d685a725a511b8dbee?pvs=4)

[Directory Manual](https://rogue-impatiens-fb5.notion.site/Directory-Manual-998424c680cd483caf8f0203b6e56a05?pvs=4)

## 📂Dataset: ****VinDr-RibCXR****

- Train dataset: 4,500
- Validation dataset: 500



## 🚀Model: Unet



**ref.** https://github.com/qubvel/segmentation_models.pytorch

**Base model:** Unet

- backbone: Efficientnet b0
- 2차 Developed model: Attention UNet
- 3차 Developed model: Attention Unet + residual block
- 4차 Developed model: Unet + residual block

**Output:**

총 20개의 segmented mask가 1장씩 나옴 → 이를 모두 합치면 ⇒ **512x512x20** 사이즈의 이미지

**Train Setup**
- optimizer: adamW (eps: 1e-6)

- base learning_rate: 1e-3

- loss function: dice loss function

- epoch: 200

- batch size: 8

- augmentation: HorizontalFlip, shiftscalerotate

## ✅ Modules



**1. Attention module: scSE**

**2. Data Preprocessing** : Gaussian blur,  CLAHE
    ![Untitled](./img/Untitled%201.png)
    
**3. Change Convolution block to “Residual”**

- **encoder에만 삽입**
  
        
- **decoder에만 삽입**

        
- **encoder+decoder 모두 삽입**


## 💯 Results

