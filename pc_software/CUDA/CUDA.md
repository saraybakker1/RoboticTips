# Tips and trics regarding CUDA:
All these tips and trics are tried in Ubuntu22.

## Installing:

## Regular problems:
### "torch._C._cuda_init() RuntimeError: No CUDA GPUs are available" ####
Navigate to *Additional drivers*, and try switching to another driver.
E.g. *Using NVIDIA driver metapackage from nvidia-driver-545 (proprietary)* instead of *(Using NVIDIA driver metapackage from nvidia-driver-535 (proprietary)*. 
