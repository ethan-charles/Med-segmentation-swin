# Advancements in Medical Segmentation: Comparative Analysis of MedSegDiff-V2 and Swin UNETR in Brain and Skin Image Processing

**Authors**: Tianxing Ma, Yichen Lu, Dianze Li, Beining Zhu  
**Affiliation**: Department of Electrical Engineering and Computer Science, University of Michigan, Ann Arbor, MI 48105  
**Emails**: {tianxinm, nechy, dianzeli, bxz}@umich.edu

## Abstract
This paper introduces MedSegDiff-V2, a novel model combining diffusion probabilistic models with vision transformers, tailored for medical imaging. Validated on brain imaging datasets, we extend its application to dermatological imaging to assess its generalization capabilities. MedSegDiff-V2 excels in handling ambiguous boundaries and complex patterns, often challenging in medical images. This study demonstrates significant enhancements in segmentation precision, emphasizing its potential utility in clinical settings.

Our paper is HERE: [Advancements in Medical Segmentation: Comparative Analysis of MedSegDiff-V2 and Swin UNETR in Brain and Skin Image Processing](https://github.com/ethan-charles/Med-segmentation-swin/blob/main/Advancements%20in%20Medical%20Segmentation%20Comparative%20Analysis%20of%20MedSegDiff-V2%20and%20Swin%20UNETR%20in%20Brain%20and%20Skin%20Image%20Processing.pdf)


# SwinUNETR: Model Overview
This repository contains the code for [Swin UNETR](https://arxiv.org/pdf/2201.01266.pdf) [1,2] for the task of brain tumor  segmentation using the [BraTS 21](http://braintumorsegmentation.org/) challenge dataset [3,4,5,6]. Swin UNETR ranked among top-perfoming models in BraTS 21 validation phase. The architecture of Swin UNETR is demonstrated as below
![image](https://github.com/ethan-charles/Med-segmentation-swin/blob/main/swinUNETR/assets/swin_unetr.png)

# MedSegDiff: Medical Image Segmentation with Diffusion Model
MedSegDiff a Diffusion Probabilistic Model (DPM) based framework for Medical Image Segmentation. The algorithm is elaborated on our paper [MedSegDiff: Medical Image Segmentation with Diffusion Probabilistic Model](https://arxiv.org/abs/2211.00611) and [MedSegDiff-V2: Diffusion based Medical Image Segmentation with Transformer](https://arxiv.org/pdf/2301.11798.pdf).

<img align="left" width="170" height="170" src="https://github.com/WuJunde/MedSegDiff/blob/master/medsegdiff_showcase.gif"> Diffusion Models work by destroying training data through the successive addition of Gaussian noise, and then learning to recover the data by reversing this noising process. After training, we can use the Diffusion Model to generate data by simply passing randomly sampled noise through the learned denoising process.In this project, we extend this idea to medical image segmentation. We utilize the original image as a condition and generate multiple segmentation maps from random noises, then perform ensembling on them to obtain the final result. This approach captures the uncertainty in medical images and outperforms previous methods on several benchmarks.


## A Quick Overview 

|<img align="left" width="480" height="170" src="https://github.com/WuJunde/MedSegDiff/blob/master/framework.png">|<img align="right" width="450" height="270" src="https://github.com/WuJunde/MedSegDiff/blob/master/frameworkv2.png">|
|:--:|:--:| 
| **MedSegDiff-V1** | **MedSegDiff-V2** |
