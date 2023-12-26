# Progressive-GAN-pytorch
A pytorch implementation of Progressive-GAN that is actually work, readable and simple to customize

A fork of [this repo](https://github.com/odegeasslbc/Progressive-GAN-pytorch) with some features added

## How to run
To start a training, just run:
```
python train.py --path /path/to/image-folder
```
An example with more configuration can be:
```
python train.py --path /path/to/imagefolder --trial_name experiment-1 --z_dim 100 --channel 512 --batch_size 4 --init_step 2 --total_iter 300000 --pixel_norm --tanh
```
For a comprehensive explanation of all the parameters, run:
```
python train.py --help
```
  
Each new running of the code will create a new folder with the specified trail_name, all the generated images, model checkpoints and loss value loging file will be stored in this new folder. A copy of the codes that you run will also be intimately stored (because you might have modefied them).

## Dataset
This code is ready for your own image datasets with the **torchvision.datasets.ImageFolder** module.  
Place all your images in a way like:
```
<image_root_folder>
        |--<subfolder 1>
                |--image 1
                |--image 2 ...
        |--<subfolder 2>
        ...
```

## Reference
1. *Progressive Growing of GANs for Improved Quality, Stability, and Variation*, **Tero Karras** (NVIDIA), **Timo Aila** (NVIDIA), **Samuli Laine** (NVIDIA), **Jaakko Lehtinen** (NVIDIA and Aalto University) [Paper (NVIDIA research)](http://research.nvidia.com/publication/2017-10_Progressive-Growing-of)
2. This implementation is based on: https://github.com/rosinality/progressive-gan-pytorch
