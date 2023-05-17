# AutoDenoise: Automatic Data Instance Denoising for Recommendations

Source code of [AutoDenoise: Automatic Data Instance Denoising for Recommendations](https://doi.org/10.1145/3543507.3583339).

![](/AutoDenoise.jpg)

## Abstract

Historical user-item interaction datasets are essential in training modern recommender systems for predicting user preferences. However, the arbitrary user behaviors in most recommendation scenarios lead to a large volume of noisy data instances being recorded, which cannot fully represent their true interests. While a large number of denoising studies are emerging in the recommender system community, all of them suffer from highly dynamic data distributions. In this paper, we propose a Deep Reinforcement Learning (DRL) based framework, AutoDenoise, with an Instance Denoising Policy Network, for denoising data instances with an instance selection manner in deep recommender systems. To be specific, AutoDenoise serves as an agent in DRL to adaptively select noise-free and predictive data instances, which can then be utilized directly in training representative recommendation models. In addition, we design an alternate two-phase optimization strategy to train and validate the AutoDenoise properly. In the searching phase, we aim to train the policy network with the capacity of instance denoising; in the validation phase, we find out and evaluate the denoised subset of data instances selected by the trained policy network, so as to validate its denoising ability. We conduct extensive experiments to validate the effectiveness of AutoDenoise combined with multiple representative recommender system models.

## Training

Run the following code to conduct the two-phase optimization:

``` python
python main.py --model_name dfm --dataset_name movielens1M --pretrain_epoch 4 --select_ratio 0.98
```

## Citation

Please cite with the below bibTex if you find it helpful to your research.
```
@inproceedings{lin2023autodenoise,
  title={AutoDenoise: Automatic Data Instance Denoising for Recommendations},
  author={Lin, Weilin and Zhao, Xiangyu and Wang, Yejing and Zhu, Yuanshao and Wang, Wanyu},
  booktitle={Proceedings of the ACM Web Conference 2023},
  pages={1003--1011},
  year={2023}
}
```
