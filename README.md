# Installation guideline for NVIDIA GPU acceleration with Tensorflow
#### Update & Upgrade
```
sudo apt update; sudo apt upgrade
```

#### Remove previously installed NVIDIA-related packages
```
sudo apt-get remove --purge '^nvidia-.*'
```

#### Install the system-recommended drivers (including NVIDIA's)
```
sudo ubuntu-drivers autoinstall
```

#### Reboot
```
sudo reboot
```

#### Check if NVIDIA driver has been installed
```
nvidia-smi
```

#### Install the toolkit
```
sudo apt install nvidia-cuda-toolkit
```
Note: If it says the the system recommended NVIDIA driver above that will be REMOVED, let it be. This issue will be fixed later.

#### Check if CUDA is installed
```
nvcc -V
```

#### Fix the above issue which replaced the system recommended NVIDIA driver
```
sudo apt install cuda
```

#### Download cuDNN .deb file
Download [here](https://developer.nvidia.com/rdp/cudnn-download). Choose the version which matches the one in top-right of `nvidia-smi` result.
```
sudo apt update
sudo apt install libcudnn8
sudo apt install libcudnn8-dev
sudo apt install libcudnn8-samples
```

#### Check if Tensorflow could utilize GPU
Create a simple model with high training epochs. Check to GPU usage with:
```
nvtop
```

Special thanks to (this guide)[https://gist.github.com/denguir/b21aa66ae7fb1089655dd9de8351a202] which helped me a lot.
If your issue persists, I highly recommend trying this.
