
<p align="center">
  <img src="https://user-images.githubusercontent.com/10940214/165389235-1d5a8994-b0c4-49b0-8ffb-a29f4062f355.png" width=200/>
  <img src="https://user-images.githubusercontent.com/10940214/165389618-63e6b369-76cd-4880-9582-360c58c8675d.png" width=200/>
</p>

# How to get quick and performant model for your edge application. _From data to application._

## Organizers:

[Paula Ramos](https://www.linkedin.com/in/paula-ramos-41097319/), [Raymond Lo](https://www.linkedin.com/in/raymondlo84/), [Helena Kloosterman](https://github.com/helena-intel), [Samet Akcay](https://www.linkedin.com/in/sametakcay/), [Zhuo Wu](https://www.linkedin.com/in/wuzhuo/) & [Yury Gorbachev](https://www.linkedin.com/in/yurygorbachev/)


## Overview:

One of the most important technology shifts of recent times is to use edge processing to collect, process, analyze and make decisions on-site or send data to the cloud. In addition, the increasing connection of millions or billions of sensors to the cloud will have a huge impact on bandwidth consumption, which will make low-latency applications unfeasible in the cloud. So, thinking about intermediate or full processing at the edge and sending reduced information to the cloud would reduce the impact on data transfer/processing, with another possible solution being the emerging 5G networks [1]. Currently, Intel through its OpenVINO toolkit contributes mostly generating low latency computing systems at the edge, while retaining the same accuracy as the original models. [2]. 

![image](https://user-images.githubusercontent.com/10940214/170517509-7d76b023-182c-4cf4-ae0c-eac8e1ca61ef.png)

_Figure 1. Optimization pipeline for deep learning models_

Not all deep learning (DL) models have been designed to run on the resource-constrained edge. Most deep neural networks (DNNs) have been designed to achieve the highest possible accuracy, without considering a trade-off between performance and accuracy to develop more computationally efficient DLs [3]. A common approach provided by most DL frameworks to accelerate inference is, to quantize a model to INT8 precision [4] and to consider a matrix multiplication reduction (sparsity) to obtain good results [5]. OpenVINO Toolkit offers several tools for making a model run faster and take less memory: Model Optimizer, Post-training Optimization Tool (POT), and Neural Network Compression Framework (NNCF). However, these good results also will depend on the dataset distribution you are using in between, training, testing, and validation. To address these challenges, OpenVINO has developed a convenient environment (OpenVINO Training Extensions OTE) (Figure 1) to train a new model with more efficient architecture using your own dataset, keeping the distribution of itself and getting the best possible results to deploy your model into the edge [6], achieving a 3.6x increase in processing speed compared to the original FP16 model (SSD-300) [5]. 

## Prework:
You would need a computer (laptop/tablet) with an [Intel Core Processor](https://docs.openvino.ai/latest/openvino_docs_OV_UG_supported_plugins_Supported_Devices.html). Alternatively, you could access the Intel hardware via [Intel DevCloud for the Edge](https://www.intel.com/content/www/us/en/developer/tools/devcloud/edge/learn/tutorials.html?s=Newest). Also, we recommend participants to be familiar with basic concepts of computer vision and deep learning, such as convolutional neural networks and PyTorch and TensorFlow frameworks. Note: A laptop with a built-in webcam is a plus for testing out the interactive demos.

1. Follow the instructions on this Wiki page https://github.com/openvinotoolkit/openvino_notebooks/wiki
2. Run the notebooks [301](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/301-tensorflow-training-openvino) and [401](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/401-object-detection-webcam)
3. Share screenshoots of your results in our repository. Discussion thread [CVPR - Prework](https://github.com/openvinotoolkit/openvino_notebooks/discussions/568)

### We will have some prizes at the end of the tutorial for whom make this prework.

![image](https://user-images.githubusercontent.com/10940214/172610882-00fbf95e-2c68-4bba-b7cd-61edd7d9af0c.png)
_Figure 2. Installation steps for Windows_


## Outline

1. Prework – OpenVINO Notebooks installation. 
2. General aspects of OpenVINO.
   - Hands-on experience – OpenVINO Notebooks. [Exercise 1](https://github.com/paularamo/cvpr-2022/blob/gh-pages/exercises/Exercise_1.md)
3. General Aspects of Optimization process
   - Model Optimizer. [Exercise 2](https://github.com/paularamo/cvpr-2022/blob/gh-pages/exercises/Exercise_2.md)
   - Post training Optimization. [Exercise 3](https://github.com/paularamo/cvpr-2022/blob/gh-pages/exercises/Exercise_3.md)
   - NNCF with segmentation model. [Exercise 4](https://github.com/paularamo/cvpr-2022/blob/gh-pages/exercises/Exercise_4.md)
   - Improve performance with AUTO plugin. [Exercise 5](https://github.com/paularamo/cvpr-2022/blob/gh-pages/exercises/Exercise_5.md)
4. OpenVINO Training Extensions (OTE).
   - Object Detection with OTE. [Exercise 5](https://github.com/paularamo/cvpr-2022/blob/gh-pages/exercises/Exercise_6.md)
5. Anomalib by OpenVINO.
   - End2End experience. Evaluate and deploy your solution using Anomalib. [Exercise 6](https://github.com/paularamo/cvpr-2022/blob/gh-pages/exercises/Exercise_7.md)


## References 
[1] Y. Ai, M. Peng and K. Zhang, "Edge computing technologies for Internet of Things: a primer," Digital Communications and Networks, 2017. 

[2] Intel Corporation, "OpenVINO™ toolkit Documentation," Intel Corporation, 2021. [Online]. Available: https://docs.openvino.ai. [Accessed 9 12 2021].

[3] A. Kozlov, I. Lazarevich and V. Shamporov, "Neural Network Compression Framework for fast model inference," arXiv, p. 13, 2020. https://arxiv.org/abs/2002.08679

[4] Pytorch, "QUANTIZATION," Torch Contributors, 2019. [Online]. Available: https://pytorch.org/docs/stable/quantization.html. [Accessed 9 12 2021].

[5] A. Kozlov, M. Kaglinskaya, I. Lazarevich, A. Dokuchaev and Y. Gorbachev, "Model Optimization Pipeline for Inference Speedup with OpenVINO™ Toolkit," Intel Corporation, 31 January 2021. [Online]. Available: https://www.intel.com/content/www/us/en/artificial-intelligence/posts/model-optimization-pipeline-with-openvino-toolkit.html. [Accessed 9 12 2021].

[6] Intel Corporation, "OpenVINO™ Training Extensions," Intel Corporation, 2021. [Online]. Available: https://github.com/openvinotoolkit/training_extensions. [Accessed 9 12 2021].


