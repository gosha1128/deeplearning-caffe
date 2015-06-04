# deeplearning-caffe

Instructions and various examples for the deep learning, caffe style...

[ This is a work in progress so bear with me...]

# Installation MACOS Yosemite

## Prerequisites

* install brew for MACOS
* make sure to update your brew installation
```
brew update
```
* install openblas
```
brew install homebrew/science/openblas
```
* install anaconda python
* install nvidia toolkit
```
https://developer.nvidia.com/cuda-downloads
```
* set env var
```
/usr/local/cuda/lib:$HOME/anaconda/lib:/usr/local/lib:/usr/lib
```
* install some post cuda dependencies
```
brew install --fresh -vd snappy leveldb gflags glog szip lmdb
brew tap homebrew/science
brew install hdf5 opencv
```
