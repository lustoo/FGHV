# FGHV

Code will be released on https://github.com/Tencent/TFace/tree/master/security/tasks/Face-Anti-Spoofing

<a href=https://arxiv.org/pdf/2112.14894.pdf>Impelmentation for paper Feature Generation and Hypothesis Verification for Reliable Face Anti-Spoofing</a>

(AAAI 2022)

Shice Liu, Shitao Lu, Hongyi Xu, Jing Yang, Shouhong Ding, Lizhuang Ma

Youtu Lab, Tencent, Shanghai, China

East China Normal University, Shanghai, China 

Shanghai Jiao Tong University, Shanghai, China

(Official PyTorch Implementation)

## Abstract

Although existing face anti-spoofing (FAS) methods achieve high accuracy in intra-domain experiments, their effects drop severely in cross-domain scenarios because of poor gener- alization. Recently, multifarious techniques have been ex- plored, such as domain generalization and representation dis- entanglement. However, the improvement is still limited by two issues: 1) It is difficult to perfectly map all faces to a shared feature space. If faces from unknown domains are not mapped to the known region in the shared feature space, acci- dentally inaccurate predictions will be obtained. 2) It is hard to completely consider various spoof traces for disentangle- ment. In this paper, we propose a Feature Generation and Hy- pothesis Verification framework to alleviate the two issues. Above all, feature generation networks which generate hy- potheses of real faces and known attacks are introduced for the first time in the FAS task. Subsequently, two hypothesis verification modules are applied to judge whether the input face comes from the real-face space and the real-face distribu- tion respectively. Furthermore, some analyses of the relation- ship between our framework and Bayesian uncertainty esti- mation are given, which provides theoretical support for reli- able defense in unknown domains. Experimental results show our framework achieves promising results and outperforms the state-of-the-art approaches on extensive public datasets.

<div align=center>

<img src="https://github.com/lustoo/FGHV/blob/main/figures/main_framework.jpg" width = "850"  />

</div>

## Experiments 

Comparison to face anti-spoofing methods on the cross-dataset testing task for domain generalization:

<div align=center>

<img src="https://github.com/lustoo/FGHV/blob/main/figures/table_four.png" width = "600"  />

</div>

Comparison to face anti-spoofing methods on the cross-type testing task for domain generalization:

<div align=center>

<img src="https://github.com/lustoo/FGHV/blob/main/figures/table_siwm.png" width = "850"  />

</div>

## Visualization

The t-SNE visualization of the face feature:

<div align=center>

<img src="https://github.com/lustoo/FGHV/blob/main/figures/tsne.jpg" width = "600"  />

</div>

## Requirements

- Python 3.6 
- Pytorch 1.5.0
- Cuda 10.1
- Python packages: `pip install numpy opencv-python wandb easydict omegaconf timm albumentations lmdb`

## Training

To run the train file in distributedDataParallel model :

`sh ./train.sh GPU_NUM CONFIG_PATH PORT`

## Citation

Please consider citing our paper in your publications if the project helps your research. BibTeX reference is as follow.

```
@inproceedings{Liu_2022_AAAI,
  title={Feature Generation and Hypothesis Verification for Reliable Face Anti-Spoofing},
  author={Shice Liu, Shitao Lu, Hongyi Xu, Jing Yang, Shouhong Ding, Lizhuang M},
  booktitle={Thirty-Sixth AAAI Conference on Artificial Intelligence (AAAI)},
  year={2022}
}

```



