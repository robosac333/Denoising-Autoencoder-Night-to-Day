# Denoising Autoencoder Night to Day
 
![alt text](day2night_.png)

### Citation
```
@InProceedings{Punnappurath_2022_CVPR,
author = {Punnappurath, Abhijith and Abuolaim, Abdullah and Abdelhamed, Abdelrahman and Levinshtein, Alex and Brown, Michael S.},
title = {Day-to-night Image Synthesis for Training Nighttime Neural ISPs},
booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
year = {2022},
}
```
### Get started
- The code was tested on Ubuntu 16.04, Python3.7, CUDA 10.1, cuDNN 8.0, Pytorch 1.7.0
- The code may work in other environments
- Requirements
  - opencv-python 
  - scipy 
  - exifread 
  - rawpy 
  - colour_demosaicing 
  - matplotlib 
  - tensorboard 
  - scikit-image==0.15.0 
- Download the dataset [[link]](https://ln5.sync.com/dl/ad8546d50#2atz8rpn-gjq5s8dq-u2revfvg-q2egqetr), and copy to `./dataset/` 
- (Optional) Download pre-trained models [[link]](https://ln5.sync.com/dl/aaba12730#hwyf4g96-ibtjtpid-qsr5rdzt-nvkz2tas), and copy to `./models/`

### Convert day images to synthetic nighttime images
- `python3 prepare_data.py --savefoldername night --dim --relight --relight_local`
- Synthetic nighttime images will be saved to `synthetic_datasets/night`
- Note: While synthesizing our nighttime images, we have also added a few *saturated lights* to mimic light bulbs in nighttime scenes (see the parameter `num_sat_lights` in `prepare_data.py`). Although not mentioned in our paper, we found that adding saturated lights yeilds slightly improved performance
- If you wish to skip generating the images, you can download our pre-generated data [[link]](https://ln5.sync.com/dl/e6db40570#hdqmmykq-fy5bwe4k-8tjsbf53-zxq34ff5), and copy to `./synthetic_datasets/night`

### Train Night Mode ISP on synthetic nighttime images

### Test the synthetic nighttime data model

### Test using our pretrained synthetic nighttime data model
