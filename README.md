# Deep Meta Metric Learning (DMML)
This repo contains PyTorch code for ICCV'19 paper: Deep Meta Metric Learning, including person re-identification experiments on Market-1501 and DukeMTMC-reID datasets.

## Requirements
- Python 3.6+
- PyTorch 0.4
- tensorboardX 1.6

To install all python packages, please run the following command:
```
pip install -r requirements.txt
```

## Datasets
### Downloading
- Market-1501 dataset can be downloaded from [here](http://www.liangzheng.org/Project/project_reid.html).
- DukeMTMC-reID dataset can be downloaded from [here](http://vision.cs.duke.edu/DukeMTMC/).
### Preparation
After downloading the datasets above, move them to the `datasets/` folder in the project root directory, and rename dataset folders to 'market1501' and 'duke' respectively. I.e., the `datasets/` folder should be organized as:
```
|-- market1501
    |-- bounding_box_train
    |-- bounding_box_test
    |-- ...
|-- duke
    |-- bounding_box_train
    |-- bounding_box_test
    |-- ...
```

## Usage
### Training
After preparing the datasets, simply run the following command to train DMML on Market-1501:
```
bash demo.sh
```
Usage instructions of all training parameters can be found in `config.py`.
### Evaluation
To evaluate the performance of a trained model, run
```
python eval.py
```
which will output Rank-1, Rank-5, Rank-10 and mAP scores.

## Trained models

[BaiduYun](https://pan.baidu.com/s/1ZaVjg3L-tmoEGu_WGC3xDQ) with extraction code: grb4.

## Citation
Please use the citation provided below if it is useful to your research:

Guangyi Chen, Tianren Zhang, Jiwen Lu, and Jie Zhou. Deep meta metric learning. In *ICCV*, 2019.
```
@inproceedings{chen2019deep,
  title={Deep meta metric learning},
  author={Chen, Guangyi and Zhang, Tianren and Lu, Jiwen and Zhou, Jie},
  booktitle={ICCV},
  year={2019}
}
```
