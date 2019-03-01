### Solo Mining HTMLCOIN via Nvidia GPU

## NVIDIA CUDA

![Nvidia](./images/nvidia.png)

First configure [HTMLCOIN wallet for solo mining](./html-daemon.md)

Once running, get ccminer from mghtthr: [https://github.com/mghtthr/ccminer](https://github.com/mghtthr/ccminer)

You must compile yourself at this time.

To solo mine, run this ccminer command:

`ccminer.exe -a htmlcoin -o http://127.0.0.1:4889 -u user -p password --no-stratum`

If you get *invalid device symbol*, your GPU is too old. Try bfgminer with OpenCL instead.