
## The MXNet Implementation of Face Age and Gender Estimation

This repository contains a lightweight model for face age and gender estimation. The model is very small and efficient about 1MB size, 10ms on single CPU core. Gender accuracy 96% on validation set and 4.1 age MAE.

Two methods ([MTCNN](https://github.com/deepinx/mtcnn-face-detection) and [ESSH](https://github.com/deepinx/enhanced-ssh-mxnet)) are both provided in this repository for face detection and alignment. For easy cases, the results of two methods are almost the same, however, on hard cases the ESSH method has a much better detection results. You can use ``python test.py --det 0`` to choose MTCNN method, or use ``python test.py --det 1`` for ESSH.

## Environment

This repository has been tested under the following environment:

-   Python 2.7 
-   Ubuntu 18.04
-   Mxnet-cu90 (==1.3.0)

## Installation

1.  Prepare the environment.

2.  Clone the repository.
    
3.  Type  `make`  to build necessary cxx libs.

## Testing

  -  Download the ESSH model from [baiducloud](https://pan.baidu.com/s/1sghM7w1nN3j8-UHfBHo6rA) or [googledrive](https://drive.google.com/open?id=1eX_i0iZxZTMyJ4QccYd2F4x60GbZqQQJ) and place it in *`./ssh-model/`*.

  -  You can use `python test.py` to test the pre-trained models.

## Training

  You can use `python train.py` to train your own models.
  
  Training datasets will come soon.
 

## Results
![Estimation Result](https://raw.githubusercontent.com/deepinx/age-gender-estimation/master/sample-images/detection%20result_test1_22.02.2019.png)

## License

MIT LICENSE

## Acknowledgment

The code is adapted based on an intial fork from the [insightface](https://github.com/deepinsight/insightface) repository.

