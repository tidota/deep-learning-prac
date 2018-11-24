# Personal practice of deep learning

This is a collection of jupyter notebook files for my personal study of deep learning.

In addition to jupyter notebook and python3, tensorflow(-gpu) and cuda are necessary.

[How to install Tensorflow GPU with CUDA 10.0 for python on Ubuntu](https://www.python36.com/how-to-install-tensorflow-gpu-with-cuda-10-0-for-python-on-ubuntu/)

# List of notes

- [CPU/GPU test by tensorflow](./tensorflow_test.ipynb): Test code of tensorflow to compare CPU and GPU.

# Troubleshooting

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

