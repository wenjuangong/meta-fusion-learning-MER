# meta-fusion-learning-MER

This repository contains the code for the method proposed in "Meta-fusion Learning Based Micro-expression Recognition".

In this work, we propose a meta-fusion learning method for effective micro-expression recognition. The proposed method is based on meta learning, which is specifically designed for few-shot learning.

## Main Results



#### Performance Comparisons between the Proposed Meta-fusion Learning (MFL) Method and the State-of-the-art Methods

method|CASME|CASME II|SMIC
:-:|:-:|:-:|:-:
LBP-SIP| 0.3684|0.4656|0.4212|
FHOFO|0.6599|0.5586|0.5122|
FR ||0.6285|0.579|
LGCcon |0.6082|0.6502||
3DFCNN |0.5444| 0.5911|0.5549|
MFL_Macro|0.6051| 0.5743|0.5244|
MFL_Micro|0.6815| 0.6104|0.6220|

#### The 4-category Classification Results on the CASME II Dataset

method|The CASME II Dataset
:-:|:-:
DTCM | 0.7206 |
MFL_Micro |0.7733|






## Running the code

### Preliminaries

**Environment**
- Python 3.7.3
- Pytorch 1.2.0
- tensorboardX
- scipy
- seaborn
- sklearn

**Datasets**
- [CASME](http://fu.psych.ac.cn/CASME/casme.php) 
- [CASME II](http://fu.psych.ac.cn/CASME/casme2.php) 
- [SMIC](http://www.cse.oulu.fi/SMICDatabase)

Download the datasets and link the folders into `Data/` or `data1/`.




### 1. Pretraining
```
python train_classifier.py --config configs/train_classifier_mini.yaml
```



### 2. Meta-fusion Module
```
python train_meta.py --config configs/train_meta_mini.yaml
```



