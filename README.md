# rotation-net
adaption of [HomographyNet](https://arxiv.org/pdf/1606.03798.pdf) (regression head) by DeTone et al. for learning rotations of images with tensorflow

![homography net architecture](resources/homographynet.png "HomographyNet")

## Content of repo
### Image Pairs Generation
[01_data_generation.ipynb](01_data_generation.ipynb) cut out grayscale patch A from MS COCO image and randomly rotate patch A between -180° and 180° to get patch B

![image pair sample](resources/image_pairs_sample.png "Image Pair Sample")

### Training
[02_network_training.ipynb](02_network_training.ipynb) train and evaluate HomographyNet with train and val image pairs

![model loss](resources/model_loss.png "Model Loss")

### Test
[03_network_inference.ipynb](03_network_inference.ipynb) test rotation error
* mean rotation error: 4.1°
* median rotation error: 2.5°

![historgram with rotation error](resources/hist_rotation_error.png "Rotation Error")

## Prerequisites
* download [MS COCO dataset](https://cocodataset.org/#download) (train/val/test) and unzip to ```data/``` folder
* (optional) download trained model [here](https://drive.google.com/drive/folders/1UBh2fX9am77awOvVaEN2x_tiD78i2fWd?usp=sharing)

## Credits
* [mazenmel/Deep-homography-estimation-Pytorch](https://github.com/mazenmel/Deep-homography-estimation-Pytorch) (data generation)
* [richard-guinto/homographynet](https://github.com/richard-guinto/homographynet) (tensorflow implementation)