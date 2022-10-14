# MADN Installation
My Platform:
   Ubuntu 20.04
   i7-12700K
   RTX 3090 Ti
   Nvidia Driver 515.65.01
   CUDA 11.4
## 1. Install Anaconda3
See [https://www.anaconda.com/](https://www.anaconda.com/)
## 2. Create Python Environment in Anaconda
```sh
conda activate
conda create -n MADN python=3.6
conda activate MADN
# Suppose you have installed CUDA 11.3/11.4/11.5
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
conda install scikit-image
conda isntall tqdm
pip install opencv-python -i https://pypi.tuna.tsinghua.edu.cn/simple
pip install natsort -i https://pypi.tuna.tsinghua.edu.cn/simple
```
## 3. Dataset Configuration
You should download RESIDE dataset firstly, then change the dataset directory in test.py(line 40):
```pyhton
      test_set = TestDatasetFromFolder4('/home/omnisky/4t/RESIDE/RTTS/RTTS')#
```