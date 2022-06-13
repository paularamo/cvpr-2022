## Exercise 7: End2End demo using Anomalib

_Goal_: Understand the Anomalib funtionality. 

_Repository_: https://github.com/openvinotoolkit/anomalib

### Final Task:

1. After CVPR, install Anomalib in your laptop https://github.com/openvinotoolkit/anomalib. Windows 10/11 and Ubuntu are supported. If you have any issue with the installation please use Anomalib repository to make your questions.
2. Download [MVTec AD DataSet](https://www.mvtec.com/company/research/datasets/mvtec-ad)
3. Run [this notebook](https://github.com/openvinotoolkit/anomalib/blob/development/notebooks/001-getting-started/001-getting-started.ipynb) in the Anomalib environment.
4. Create your own data.
5. Modify the dataset section of your config.yaml file in this way:

```
# Replace the dataset configs with the following.
dataset:
  name: <your_dataset_name>
  format: folder
  path: ./datasets/<your_dataset_name> #dataset folder should be in the root folder of anomalib
  normal_dir: normal # name of the folder containing normal images.
  abnormal_dir: abnormal # name of the folder containing abnormal images.
  task: classification # classification or segmentation
  mask: null #optional
  normal_test_dir: null # optional
  extensions: null
  split_ratio: 0.2  # normal images ratio to create a test split
  seed: 0
  image_size: 256
  train_batch_size: 32
  test_batch_size: 32
  num_workers: 8
  transform_config:
    train: null
    val: null
  create_validation_set: true
  tiling:
    apply: false
    tile_size: null
    stride: null
    remove_border_count: 0
    use_random_tiling: False
    random_tile_count: 16

```
5. Don't run the cells with mask_images variables.
6. Show us your anomaly detection, sharing with us your result using this Discussion thread, using "Final Task" and your name in the header message.
https://github.com/openvinotoolkit/openvino_notebooks/discussions/569

We will announce prizes for this Final task on Social Media, so stay connected with us.


Paula Ramos https://www.linkedin.com/in/paula-ramos-41097319/

Raymond Lo https://www.linkedin.com/in/raymondlo84/

----------------------------------------------------------------------------------------------------------------
### For your reference, see this [link](https://doi.org/10.48550/arxiv.2202.08341)
