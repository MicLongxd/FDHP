# FDHP
A novel hybrid self centered prediction framework based on driving feature embedding implementation
# Introduction
This is a Pytorch implementation of the model described in our paper:
    Xiangdong Long, He Zhang, Tianyu Liang and Shuqin Wang. FDHP:A novel hybrid self centered prediction framework based on driving feature embedding implementation.
# Dependencies
    PyTorch ≥ 1.0.1
    CUDA 9.0.176
    CuDNN 7.4.2
    Python 3.6.8

# Data
### EPIC-Kitchens dataset

For the raw data of the EPIC-Kitchens dataset, please refer to https://github.com/epic-kitchens/download-scripts to download.

For the three modality features (rgb, flow, obj), please refer to https://github.com/fpv-iplab/rulstm to download. After downloading, put them in the folder './data'.

### EGTEA Gaze+ dataset

For the raw data of the EGTEA Gaze+ dataset, please refer to http://cbs.ic.gatech.edu/fpv/ to download.

For the extracted features, please refer to https://github.com/fpv-iplab/rulstm to download. After downloading, put them in the folder './data'.

### 50 Salads dataset

For the raw data of the 50 Salads dataset, please refer to http://cvip.computing.dundee.ac.uk/datasets/foodpreparation/50salads/ to download.

For the extracted features, please refer to https://github.com/colincsl/TemporalConvolutionalNetworks to download. After downloading, put them in the folder './data'.

### Breakfast dataset

For the raw data of the Breakfast dataset, please refer to https://serre-lab.clps.brown.edu/resource/breakfast-actions-dataset/ to download.

For the extraced I3D features, please download from Baidu passward: 'wub3' or Google Drive. After downloading, put them in the folder './data'.

# Training
### EPIC-Kitchens
 - For rgb feature python: main.py --gpu_ids 0 --batch_size 128 --wd 1e-5 --lr 0.1 --reinforce_verb_weight 0.01 --reinforce_noun_weight 0.01 --revision_weight 0.8 --mode train --modality rgb --hidden 1024 --feat_in 1024

Silimar commonds can be used for flow or obj features.

###  Validation for Epic-Kitchen dataset
Please download the pre-trained model weigths from Baidu passward: 'wub3' or Google Drive, and put them in the folder './results/EPIC/base_srl/pre_trained/'.

 - For rgb feature, python main.py --gpu_ids 0 --batch_size 128 --mode validate --modality rgb --hidden 1024 --feat_in 1024 --resume_timestamp pre_trained

 - For flow feature, python main.py --gpu_ids 0 --batch_size 128 --mode validate --modality flow --hidden 1024 --feat_in 1024 --resume_timestamp pre_trained*

 - For obj feature, python main.py --gpu_ids 0 --batch_size 128 --mode validate --modality obj --hidden 352 --feat_in 352 --resume_timestamp pre_trained

 - For three modality features, python main.py --gpu_ids 0 --batch_size 128 --mode validate --modality fusion --resume_timestamp pre_trained
# Citation
Please cite our paper if you use this code in your own work:

    @article{fmclxd,
      title={FDHP:A novel hybrid self centered prediction framework based on driving feature embedding implementation},
      author={Xiangdong Long, He Zhang, Tianyu Liang and Shuqin Wang},
      journal={IEEE Transactions on Pattern Analysis \& Machine Intelligence},
      number={01},
      pages={1--1},
      year={2025},
      publisher={IEEE Computer Society}
    }
