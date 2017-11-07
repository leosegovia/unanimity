

### Before install dependencies:
```
sudo apt-get update && \
sudo apt-get install build-essential software-properties-common  gfortran graphviz libjpeg-dev libfreetype6-dev -y && \
sudo add-apt-repository ppa:ubuntu-toolchain-r/test -y && \
sudo apt-get update && \
sudo apt-get install gcc-snapshot -y && \
sudo apt-get update && \
sudo apt-get install gcc-6 g++-6 -y && \
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-6 60 --slave /usr/bin/g++ g++ /usr/bin/g++-6 && \
sudo apt-get install gcc-4.8 g++-4.8 -y && \
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 60 --slave /usr/bin/g++ g++ /usr/bin/g++-4.8;
```
## Install OPENBLAS

```
sudo apt-ge t install libopenblas-* -y && \
```


Once dependencied have been installed proceed with `pitchfork`install:

### To install Individual Tools: use `pitchfork`

The easiest way to build is to use the `pitchfork` build tool, which
automates dependency fetching/resolution:

  ```sh
  git clone https://github.com/PacificBiosciences/pitchfork && \
  cd pitchfork                                              && \
  echo "HAVE_OPENBLAS = \usr" >> ./settings.mk && \
  sudo make pbccs
  ```
