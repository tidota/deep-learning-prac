# Personal practice of deep learning

This is a collection of jupyter notebook files for my personal study of deep learning.

In addition to jupyter notebook and python3, tensorflow(-gpu) and cuda are necessary.

[How to install Tensorflow GPU with CUDA 10.0 for python on Ubuntu](https://www.python36.com/how-to-install-tensorflow-gpu-with-cuda-10-0-for-python-on-ubuntu/)

# List of notes

- [CPU/GPU test by tensorflow](./tensorflow_test.ipynb): Test code of tensorflow to compare CPU and GPU.

# Troubleshooting

***Be careful when you run the commands mentioned below:*** This is just my personal notes so it could contain wrong information.

The environment:
- Machine: HP Z620
- Ubuntu 18.04
- Graphic card: Quadro K600

## Reinstallation of Nvidia driver

Sometimes a wrong nvidia driver is installed and the display setting has only one choice of rough resolution.

There may be a better way, but to the best of my knowledge, reinstallation of cuda fixes driver-related problems.
For reinstallation, you need to exit GUI and work on text-based environment (tty2 etc).

Reference: [How to install Tensorflow GPU with CUDA 10.0 for python on Ubuntu](https://www.python36.com/how-to-install-tensorflow-gpu-with-cuda-10-0-for-python-on-ubuntu/) (see "Step 6: Install NVIDIA CUDA 10.0:")

1. Switch to tty2 by Ctrl + Alt + F2
1. Log in
1. Kill GUI: `sudo service lightdm stop` (if gdm is used, `sudo service gdm stop`)
1. Run the following commands:
   ```
   sudo apt-get purge nvidia*
   sudo apt-get autoremove
   sudo apt-get autoclean
   sudo rm -rf /usr/local/cuda*
   sudo apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
   echo "deb https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64 /" | sudo tee /etc/apt/sources.list.d/cuda.list
   sudo apt-get update
   sudo apt-get -o Dpkg::Options::="--force-overwrite" install cuda-10-0 cuda-drivers
   ```
1. Reboot

## Installation by `pip3`

Resource: [Error after upgrading pip: cannot import name 'main'](https://stackoverflow.com/questions/49836676/error-after-upgrading-pip-cannot-import-name-main)

If the following message appears while installing by `pip3 install`, 
```
ImportError: cannot import name 'main'
```

Run this,
```
sudo python3 -m pip uninstall pip && sudo apt install python3-pip --reinstall
```

