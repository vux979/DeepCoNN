DeepCoNN
===
The code implementation for the paper：  
Lei Zheng, Vahid Noroozi, and Philip S Yu. 2017. Joint deep modeling of users and items using reviews for recommendation. In WSDM. ACM, 425-434.

# Environments
  + python 3.8
  + pytorch 1.70

# Dataset
  You need to prepare the following documents:  
  1. dataset(`data/Digital_Music_5.json.gz`)  
   Download from http://jmcauley.ucsd.edu/data/amazon (Choose Digital Music)  
   Preprocess origin dataset in json format to train.csv,valid.csv and test.csv.  
   ```
   python preprocess.py
   ```

  2. Word Embedding(`embedding/glove.6B.50d.txt`)  
   Download from https://nlp.stanford.edu/projects/glove

# Running

Train and evaluate the model:
```
python main.py
```
# create env
conda create -n pytorch170 python=3.8     
activate pytorch170
```bash
# CUDA 11.0
pip install torch==1.7.0+cu110 torchvision==0.8.0+cu110 torchaudio==0.7.0 -f https://download.pytorch.org/whl/torch_stable.html

# CUDA 10.2
pip install torch==1.7.0 torchvision==0.8.0 torchaudio==0.7.0

# CUDA 10.1
pip install torch==1.7.0+cu101 torchvision==0.8.0+cu101 torchaudio==0.7.0 -f https://download.pytorch.org/whl/torch_stable.html

# CUDA 9.2
pip install torch==1.7.0+cu92 torchvision==0.8.0+cu92 torchaudio==0.7.0 -f https://download.pytorch.org/whl/torch_stable.html

# CPU only
pip install torch==1.7.0+cpu torchvision==0.8.0+cpu torchaudio==0.7.0 -f https://download.pytorch.org/whl/torch_stable.html
```
