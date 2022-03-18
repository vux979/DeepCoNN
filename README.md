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
`ERROR: Could not find a version that satisfies the requirement torchvision==0.8.0+cu101 (from versions: 0.1.6, 0.1.7, 0.1.8, 0.1.9, 0.2.0, 0.2.1, 0.2.2, 0.2.2.post2, 0.2.2.post3, 0.5.0, 0.5.0+cpu, 0.5.0+cu92, 0.6.0, 0.6.0+cpu, 0.6.0+cu101, 0.6.0+cu92, 0.6.1, 0.6.1+cpu, 0.6.1+cu101, 0.6.1+cu92, 0.7.0, 0.7.0+cpu, 0.7.0+cu101, 0.8.0, 0.8.1, 0.8.1+cpu, 0.8.1+cu101, 0.8.1+cu110, 0.8.2, 0.8.2+cpu, 0.8.2+cu101, 0.8.2+cu110, 0.9.0, 0.9.0+cpu, 0.9.0+cu101, 0.9.0+cu111, 0.9.1, 0.9.1+cpu, 0.9.1+cu101, 0.9.1+cu102, 0.9.1+cu111, 0.10.0, 0.10.0+cpu, 0.10.0+cu102, 0.10.0+cu111, 0.10.1, 0.10.1+cpu, 0.10.1+cu102, 0.10.1+cu111, 0.11.0, 0.11.0+cpu, 0.11.0+cu102, 0.11.0+cu113, 0.11.1, 0.11.1+cpu, 0.11.1+cu102, 0.11.1+cu113, 0.11.2, 0.11.2+cpu, 0.11.2+cu102, 0.11.2+cu113, 0.11.3, 0.11.3+cpu, 0.11.3+cu102, 0.11.3+cu113, 0.12.0, 0.12.0+cpu, 0.12.0+cu113, 0.12.0+cu115)
ERROR: No matching distribution found for torchvision==0.8.0+cu101`
conda create -n pytorch170 python=3.8     
activate pytorch170
