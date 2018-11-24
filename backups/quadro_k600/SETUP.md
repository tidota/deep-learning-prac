# whl file of tensorflow-gpu for Quadro K600

Nvidia graphic card with 3.0 of compute capacity is not supported by the tensorflow-gpu package available in apt. Instead of apt, a package file (.whl) must be compiled from the source code. This directory contains the generated whl file. To install it, follow the instructions below.

1. download [the compiled whl file of tensorflow-gpu](https://drive.google.com/open?id=1vaNaZW90XeqPchU0fmnVW1cZXx9TkfdA)

1. install the tensorflow-gpu package

   ```
   pip3 install tensorflow*.whl
   ```

