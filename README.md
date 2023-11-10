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

