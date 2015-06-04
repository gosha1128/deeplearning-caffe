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
* install anaconda python ( set it to be the default python )
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
* install all the anaconda dependencies
```
cd python
for req in $(cat requirements.txt); do conda install $req; done
```
* set env var
```
export DYLD_FALLBACK_LIBRARY_PATH=/usr/local/cuda/lib:$HOME/anaconda/lib:/usr/local/lib:/usr/lib
```
* protobuf dependency
```
brew install --build-from-source --with-python --fresh -vd protobuf
```
* boost dependency
```
brew install --build-from-source --fresh -vd boost boost-python
```


## Compile

* setup makefile
```
cp Makefile.config.example Makefile.config
```
* edit makefile to build from Anaconda python
* make all

