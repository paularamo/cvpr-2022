## Exercise 4: Quantize a Segmentation Model and Show Live Inference

_Goal_: Understand the NNCF funtionality. Post Training Quantization

_Notebook_: 

_Action_: 
Download this [pre-trained model](https://github.com/paularamo/cvpr-2022/blob/gh-pages/unet_kits19_state_dict.pth) and locate it into ```~/openvino_notebooks/notebooks/110-ct-segmentation-quantize/pretrained_model```

Run all cells and see the perfomance on your laptop.

### Task #4:

1. Change the preset option on nncf_config to ```mixed```
2. Remember you need to load the model again before doing that, re-running all cell or or copy/paste these two lines to the nncf_config_dict cell.
```model = monai.networks.nets.BasicUNet(spatial_dims=2, in_channels=1, out_channels=1).eval()
model.load_state_dict(new_state_dict)```
3. Share with us your result using this Discussion thread, using Task # 4 and your name in the header message.
https://github.com/openvinotoolkit/openvino_notebooks/discussions/569



