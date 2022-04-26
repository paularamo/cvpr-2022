# How to get quick and performant model for your edge application. _From data to application._

## Overview:

One of the most important technology shifts of recent times is to use edge processing to collect, process, analyze and make decisions on-site or send data to the cloud. In addition, the increasing connection of millions or billions of sensors to the cloud will have a huge impact on bandwidth consumption, which will make low-latency applications unfeasible in the cloud. So, thinking about intermediate or full processing at the edge and sending reduced information to the cloud would reduce the impact on data transfer/processing, with another possible solution being the emerging 5G networks [1]. Currently, Intel through its OpenVINO toolkit contributes mostly generating low latency computing systems at the edge, while retaining the same accuracy as the original models. [2]. 

Not all deep learning (DL) models have been designed to run on the resource-constrained edge. Most deep neural networks (DNNs) have been designed to achieve the highest possible accuracy, without considering a trade-off between performance and accuracy to develop more computationally efficient DLs [3]. A common approach provided by most DL frameworks to accelerate inference is, to quantize a model to INT8 precision [4] and to consider a matrix multiplication reduction (sparsity) to obtain good results [5]. OpenVINO Toolkit offers several tools for making a model run faster and take less memory: Model Optimizer, Post-training Optimization Tool (POT), and Neural Network Compression Framework (NNCF). However, these good results also will depend on the dataset distribution you are using in between, training, testing, and validation. To address these challenges, OpenVINO has developed a convenient environment (OpenVINO Training Extensions OTE) (Figure 1) to train a new model with more efficient architecture using your own dataset, keeping the distribution of itself and getting the best possible results to deploy your model into the edge [6], achieving a 3.6x increase in processing speed compared to the original FP16 model (SSD-300) [5]. 

![image](https://user-images.githubusercontent.com/10940214/164305989-a43138e4-a0e3-45ce-8d84-980ffc18b98b.png)


_Figure 1. Optimization pipeline for deep learning models_

## Prework:
You would need a computer (laptop/tablet) with an [Intel Core Processor](https://docs.openvino.ai/latest/openvino_docs_OV_UG_supported_plugins_Supported_Devices.html). Alternatively, you could access the Intel hardware via [Intel DevCloud for the Edge](https://www.intel.com/content/www/us/en/developer/tools/devcloud/edge/learn/tutorials.html?s=Newest). Also, we recommend participants to be familiar with basic concepts of computer vision and deep learning, such as convolutional neural networks and PyTorch and TensorFlow frameworks. Note: A laptop with a built-in webcam is a plus for testing out the interactive demos.

To get started, please check the followed pre-requisites. You may follow the 10 steps instruction below to have ready the environment on your laptop. Install all pre-requisites for [Windows](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Windows), [Ubuntu](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Ubuntu), [Fedora, CentOS or RedHat](https://github.com/openvinotoolkit/openvino_notebooks/wiki/Red-Hat-and-CentOS), and [macOS](https://github.com/openvinotoolkit/openvino_notebooks/wiki/macOS)

### Prework-challenge
Pending

## Outline

1.	Motivation. Trend, edge-computing, and real-world scenarios for DL deployment and optimizations. OpenVINO, OTE, and OpenVINO Optimization.

2.	OpenVINO Training Extensions definition, architecture, and use cases. Training from scratch, Retraining, Anomalib example.

3.  OpenVINO Model Optimization with Model Optimizer, POT, and NNCF. how to integrate to train/optimize a new model using NNCF and POT. Hands-on experience. 

4.	Evaluate and deploy your solution as an edge-computing system. The real case for object detection and instance segmentation on Intel Hardware (e.g. Xenon Server Processors, Gen 12th Mobile processors, and Integrated Graphics Processors).


### References 

[1] Y. Ai, M. Peng and K. Zhang, "Edge computing technologies for Internet of Things: a primer," Digital Communications and Networks, 2017. 

[2] Intel Corporation, "OpenVINO™ toolkit Documentation," Intel Corporation, 2021. [Online]. Available: https://docs.openvino.ai. [Accessed 9 12 2021].

[3] A. Kozlov, I. Lazarevich and V. Shamporov, "Neural Network Compression Framework for fast model inference," arXiv, p. 13, 2020. https://arxiv.org/abs/2002.08679

[4] Pytorch, "QUANTIZATION," Torch Contributors, 2019. [Online]. Available: https://pytorch.org/docs/stable/quantization.html. [Accessed 9 12 2021].

[5] A. Kozlov, M. Kaglinskaya, I. Lazarevich, A. Dokuchaev and Y. Gorbachev, "Model Optimization Pipeline for Inference Speedup with OpenVINO™ Toolkit," Intel Corporation, 31 January 2021. [Online]. Available: https://www.intel.com/content/www/us/en/artificial-intelligence/posts/model-optimization-pipeline-with-openvino-toolkit.html. [Accessed 9 12 2021].

[6] Intel Corporation, "OpenVINO™ Training Extensions," Intel Corporation, 2021. [Online]. Available: https://github.com/openvinotoolkit/training_extensions. [Accessed 9 12 2021].


