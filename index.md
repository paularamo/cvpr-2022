## CVPR-2022
## How to get quick and performant model for your edge application. _From data to application._

### Course description:

One of the most important technology shifts of recent times is to use edge processing to collect, process, analyze and make decisions on-site or send data to the cloud. In addition, the increasing connection of millions or billions of sensors to the cloud will have a huge impact on bandwidth consumption, which will make low-latency applications unfeasible in the cloud. So, thinking about intermediate or full processing at the edge and sending reduced information to the cloud would reduce the impact on data transfer/processing, with another possible solution being the emerging 5G networks [1]. Currently, Intel through its OpenVINO toolkit contributes mostly generating low latency computing systems at the edge, while retaining the same accuracy as the original models. [2]. 

Not all deep learning (DL) models have been designed to run on the resource-constrained edge. Most deep neural networks (DNNs) have been designed to achieve the highest possible accuracy, without considering a trade-off between performance and accuracy to develop more computationally efficient DLs [3]. A common approach provided by most DL frameworks to accelerate inference is, to quantize a model to INT8 precision [4] and to consider a matrix multiplication reduction (sparsity) to obtain good results [5]. However, these good results also will depend on the dataset distribution you are using in between, training, testing, and validation.
To address these challenges, OpenVINO has developed a convenient environment (OpenVINO Training Extensions OTE) (Figure 1) to train a new model with more efficient architecture using your own dataset, keeping the distribution of itself and getting the best possible results to deploy your model into the edge [6], achieving a 3.6x increase in processing speed compared to the original FP16 model (SSD-300) [5]. 

![image](https://user-images.githubusercontent.com/10940214/164305989-a43138e4-a0e3-45ce-8d84-980ffc18b98b.png)


_Figure 1. Optimization pipeline for deep learning models_

The OTE environment provides different tools for quantization, pruning and sparsity. Basically, OTE uses a novel compress system called Neural Network Compression Framework (NNCF), that allows the production of compressed models that are quantized and pruned. NNCF provides a suite of advanced algorithms for Neural Networks inference optimization in OpenVINO™ with minimal accuracy drop [3]. NNCF and OTE are designed to work mainly with PyTorch and TensorFlow models, and use OpenVINO Notebooks. Users can learn, test, and build deep learning models through a high-level C++ Inference Engine API integrated with application logic [7] and [8].
This tutorial will present the optimization pipeline for OTE, how the NNCF and OTE are organized, the basic workflow, and its implementation in a real-world computer vision (CV) pipeline for image classification, object detection, and semantic segmentation. We could see different instances training, optimization, and deployment under an edge device (Figure 2).

![image](https://user-images.githubusercontent.com/10940214/164103255-95fa7f46-cdae-4aaf-b5a8-66477d7cc1a7.png)


_Figure 2. Detailed optimization pipeline for development and deployment of deep learning models with OpenVINO Training Extensions. Users can take advantages of various optimization techniques at pre- and post-training._

### Outline

1.	Motivation. Trend, edge-computing, and real-world scenarios for DL deployment and optimizations. - Deck (pending - I want also include here general aspects of OpenVINO)

2.	[OpenVINO Training Extensions definition, architecture, and use cases](https://docs.google.com/document/d/1ce4_2ifOAodHM_ZFZ42Fbj6JW-AMFBMuEXKMk3P1maA/edit).

3.  [Step-by-step tutorial on how to integrate to train a new model using OTE tools for getting significant speedup](https://github.com/openvinotoolkit/training_extensions).
    - [Training your own model your your own data](https://github.com/openvinotoolkit/training_extensions/blob/develop/ote_cli/notebooks/train.ipynb).
    - [Evaluate and test your model](https://github.com/openvinotoolkit/training_extensions/blob/eugene/dev/ote_cli/notebooks/eval.ipynb).

4.  [OpenVINO Model Optimization with Model Optimizer, POT, and NNCF](https://docs.google.com/document/d/1EpXVqIFo2YZYcJaqgck-NMyzMB-z47_6wbGyywcyTwg/edit#heading=h.fo7i3fb4o6je) - [Pending](https://docs.google.com/document/d/1iQR5OHGEw5qVj-2DN300BblVgZq5kmgt_0NlpaVFa-4/edit#heading=h.qqoojrkgtp9h)

5.	[Step-by-step tutorial on how to integrate to train/optimize a new model using NNCF and POT. Hands-on experience](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/111-detection-quantization). - Notebook (pending)

6.	Evaluate and deploy your solution as an edge-computing system. The real case for object detection and instance segmentation on Intel Hardware (e.g. Xenon Server Processors, Gen 12th Mobile processors, and Integrated Graphics Processors). - Retail example

### References 
[1] Y. Ai, M. Peng and K. Zhang, "Edge computing technologies for Internet of Things: a primer," Digital Communications and Networks, 2017. 

[2] Intel Corporation, "OpenVINO™ toolkit Documentation," Intel Corporation, 2021. [Online]. Available: https://docs.openvino.ai. [Accessed 9 12 2021].

[3] A. Kozlov, I. Lazarevich and V. Shamporov, "Neural Network Compression Framework for fast model inference," arXiv, p. 13, 2020. https://arxiv.org/abs/2002.08679

[4] Pytorch, "QUANTIZATION," Torch Contributors, 2019. [Online]. Available: https://pytorch.org/docs/stable/quantization.html. [Accessed 9 12 2021].

[5] A. Kozlov, M. Kaglinskaya, I. Lazarevich, A. Dokuchaev and Y. Gorbachev, "Model Optimization Pipeline for Inference Speedup with OpenVINO™ Toolkit," Intel Corporation, 31 January 2021. [Online]. Available: https://www.intel.com/content/www/us/en/artificial-intelligence/posts/model-optimization-pipeline-with-openvino-toolkit.html. [Accessed 9 12 2021].

[6] Intel Corporation, "OpenVINO™ Training Extensions," Intel Corporation, 2021. [Online]. Available: https://github.com/openvinotoolkit/training_extensions. [Accessed 9 12 2021].

[7] Intel Corporation, "Optimizing PyTorch models with Neural Network Compression Framework of OpenVINO by 8-bit quantization.," Intel Corporation, 2021. [Online]. 

