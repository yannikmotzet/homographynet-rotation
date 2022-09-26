# rotation-net
adaption of [HomographyNet](https://arxiv.org/pdf/1606.03798.pdf) (regression head) by DeTone et al. for learning rotations of images with tensorflow

## How it works
* image pairs generation: cut out grayscale patch from MS COCO image and randomly rotate patch between -180° and 180°
* train and evaluate HomographyNet with train and val image pairs
* test rotation error

## Prerequisites
* download [MS COCO dataset](https://cocodataset.org/#download) (train/val/test) and unzip to [data](data) folder
* (optional) download trained model [here](https://drive.google.com/drive/folders/1UBh2fX9am77awOvVaEN2x_tiD78i2fWd?usp=sharing)

## Results
* mean rotation error: 5.6°
* median rotation error: 3.6°

## Credits
* [mazenmel/Deep-homography-estimation-Pytorch](https://github.com/mazenmel/Deep-homography-estimation-Pytorch) (data generation)
* [richard-guinto/homographynet](https://github.com/richard-guinto/homographynet) (tensorflow implementation)