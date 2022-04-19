## CVPR-2022
## How to get quick and performant model for your edge application. From data to application.

### Course description (Topics, brief outline, and important details):

One of the most important technology shifts of recent times is to use edge processing to collect, process, analyze and make decisions on-site or send data to the cloud. In addition, the increasing connection of millions or billions of sensors to the cloud will have a huge impact on bandwidth consumption, which will make low-latency applications unfeasible in the cloud. So, thinking about intermediate or full processing at the edge and sending reduced information to the cloud would reduce the impact on data transfer/processing, with another possible solution being the emerging 5G networks [1]. Currently, Intel through its OpenVINO toolkit contributes mostly generating low latency computing systems at the edge, while retaining the same accuracy as the original models. [2]. 
Not all deep learning (DL) models have been designed to run on the resource-constrained edge. Most deep neural networks (DNNs) have been designed to achieve the highest possible accuracy, without considering a trade-off between performance and accuracy to develop more computationally efficient DLs [3]. A common approach provided by most DL frameworks to accelerate inference is, to quantize a model to INT8 precision [4] and to consider a matrix multiplication reduction (sparsity) to obtain good results [5]. However, these good results also will depend on the dataset distribution you are using in between, training, testing, and validation.
To address these challenges, OpenVINO has developed a convenient environment (OpenVINO Training Extensions OTE) (Figure 1) to train a new model with more efficient architecture using your own dataset, keeping the distribution of itself and getting the best possible results to deploy your model into the edge [6], achieving a 3.6x increase in processing speed compared to the original FP16 model (SSD-300) [5]. 

![image](https://user-images.githubusercontent.com/10940214/164093127-c02cbf5e-506d-490b-876c-a1be2fd39c3d.png)
Figure 1. Optimization pipeline for deep learning models

The OTE environment provides different tools for quantization, pruning and sparsity. Basically, OTE uses a novel compress system called Neural Network Compression Framework (NNCF), that allows the production of compressed models that are quantized and pruned. NNCF provides a suite of advanced algorithms for Neural Networks inference optimization in OpenVINO™ with minimal accuracy drop [3]. NNCF and OTE are designed to work mainly with PyTorch and TensorFlow models, and use OpenVINO Notebooks. Users can learn, test, and build deep learning models through a high-level C++ Inference Engine API integrated with application logic [7] and [8].
This tutorial will present the optimization pipeline for OTE, how the NNCF and OTE are organized, the basic workflow, and its implementation in a real-world computer vision (CV) pipeline for image classification, object detection, and semantic segmentation. We could see different instances training, optimization, and deployment under an edge device (Figure 2).


You can use the [editor on GitHub](https://github.com/paularamo/cvpr-2022.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/paularamo/cvpr-2022.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
