
---

<div align="center">

# An Ensemble Approach for Patient RFS Prognosis of Head and Neck Tumor Using Multimodal Data

<a href="https://pytorch.org/get-started/locally/"><img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-ee4c2c?logo=pytorch&logoColor=white"></a>
<a href="https://pytorchlightning.ai/"><img alt="Lightning" src="https://img.shields.io/badge/-Lightning-792ee5?logo=pytorchlightning&logoColor=white"></a>
<a href="https://hydra.cc/"><img alt="Config: Hydra" src="https://img.shields.io/badge/Config-Hydra-89b8cd"></a>
[![Paper](http://img.shields.io/badge/paper-arxiv.1001.2234-B31B1B.svg)](https://www.nature.com/articles/nature14539)
[![Conference](http://img.shields.io/badge/AnyConference-year-4b44ce.svg)](https://papers.nips.cc/paper/2020)

</div>

## Description
肿瘤的准确预后可以帮助医生提供适当的治疗方案，从而拯救许多人的生命。在过去的几十年里，传统的机器学习算法在制作预后模型方面非常有用。在多模态方法中利用患者表格数据，如人口统计学和患者病史，以及成像数据来解决预后任务，最近开始引起更多兴趣，并有可能创造更准确的解决方案。网络合并了深度多任务逻辑回归（MTLR）和考克斯比例危害模型（CoxPH）模型，以利用患者的临床和成像（CT和PET）数据预测头颈部肿瘤患者的预后结果。CT和PET扫描的特征与患者的电子健康记录融合并结合进行预测。

## How to run
Install dependencies
```yaml
# clone project
git clone https://github.com/Fangkangkang1126/RFS--Predict
cd your-repo-name

# [OPTIONAL] create conda environment
bash bash/setup_conda.sh

# install requirements
pip install -r requirements.txt
```

Train model with default configuration
```yaml
# data
create the data folder and copy the downloaded data to it. Also, update all the data paths in the config files. 

# default
python run.py

# train on CPU
python run.py trainer.gpus=0

# train on GPU
python run.py trainer.gpus=1
```

Train model with chosen experiment configuration from [configs/experiment/](configs/experiment/)
```yaml
python run.py experiment=experiment_name
```

You can override any parameter from command line like this
```yaml
python run.py trainer.max_epochs=20 datamodule.batch_size=64
```



<br>
# RFS--Predict
