# Decoupled Dynamic Spatial-Temporal Graph Neural Network for Traffic Forecasting

Code for our VLDB'22 paper: "[Decoupled Dynamic Spatial-Temporal Graph Neural Network for Traffic Forecasting](https://arxiv.org/abs/2206.09112)".

<img src="figures/D2STGNN.png" alt="D2STGNN" style="zoom:42%;" />

> We all depend on mobility, and vehicular transportation affects the daily lives of most of us. Thus, the ability to forecast the state of traffic in a road network is an important functionality and a challenging task. Traffic data is often obtained from sensors deployed in a road network. Recent proposals on spatial-temporal graph neural networks have achieved great progress at modeling complex spatial-temporal correlations in traffic data, by modeling traffic data as a diffusion process. However, intuitively, traffic data encompasses two different kinds of hidden time series signals, namely the diffusion signals and inherent signals. Unfortunately, nearly all previous works coarsely consider traffic signals entirely as the outcome of the diffusion, while neglecting the inherent signals, which impacts model performance negatively. To improve modeling performance, we propose a novel Decoupled Spatial-Temporal Framework (DSTF) that separates the diffusion and inherent traffic information in a data-driven manner, which encompasses a unique estimation gate and a residual decomposition mechanism. The separated signals can be handled subsequently by the diffusion and inherent modules separately. Further, we propose an instantiation of DSTF, Decoupled Dynamic Spatial-Temporal Graph Neural Network (D2STGNN), that captures spatial-temporal correlations and also features a dynamic graph learning module that targets the learning of the dynamic characteristics of traffic networks. Extensive experiments with four real-world traffic datasets demonstrate that the framework is capable of advancing the state-of-the-art.

## 1. Table of Contents

```text
configs         ->  training Configs and model configs for each dataset
dataloader      ->  pytorch dataloader
datasets        ->  raw data and processed data
model           ->  model implementation and training pipeline
output          ->  model checkpoint
```

## 2. Requirements

```bash
pip install -r requirements.txt
```

## 3. Data Preparation

### 3.1 Build Data

### 3.2 Data Process

## 4. Training the D2STGNN Model

```bash
python main.py --dataset=$DATASET_NAME
```

E.g., `python main.py --dataset=CH81`.

## 5 Loading a Pretrained D2STGNN Model

Check the config files of the dataset in `configs/$DATASET_NAME`, and set the startup args to test mode.

## 6. Citing

If you find this repository useful for your work, please consider citing it as follows:

```bibtex
@article{DBLP:journals/pvldb/ShaoZWWXCJ22,
  author    = {Zezhi Shao and
               Zhao Zhang and
               Wei Wei and
               Fei Wang and
               Yongjun Xu and
               Xin Cao and
               Christian S. Jensen},
  title     = {Decoupled Dynamic Spatial-Temporal Graph Neural Network for Traffic
               Forecasting},
  journal   = {Proc. {VLDB} Endow.},
  volume    = {15},
  number    = {11},
  pages     = {2733--2746},
  year      = {2022}
}
```

## References

[1]  Shao, Z., Zhang, Z., Wei, W., Wang, F., Xu, Y.-J., Cao, X., and Jensen, C. (2022). Decoupled dynamic spatial-temporal graph neural network for traffic forecasting. Proceedings of the VLDB Endowment, 15:2733–2746.
