# deeplearning-caffe

Instructions and various examples for the deep learning, caffe style.  These instructions will install the python and matlab bindings.  Example networks are provided.

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
* edit makefile to force CPU builds only ( no GPU support )
* make
```
make all
```
* make the tests and run them
```
make test
make runtest
```
* if the tests fail, try the following
  * (libpng) I had to use brew to update libpng to a compatible version
  * (libImath) I had to use brew to install opencv 

## Test Python bindings

* use ipython and test out some of the samples, from the caffe directory
```
~/anaconda/bin/ipython notebook examples/
<click on classification.ipynb and run the python sections>
```

## Configure For Matlab

## Test Matlab bindings


