# Install Instructions for OpenRave in OS X 10.11.3 x64

The Instructions work for branches master & latest_stable.

Info sources from:

- [OpenRave](http://openrave.org/docs/latest_stable/coreapihtml/installation_linux.html)
- [André Dietrich](http://www.aizac.info/installing-openrave0-9-on-ubuntu-trusty-14-04-64bit/)


- [Install instructions for OpenRave in Ubuntu/Ubuntu Mate 14.04.2 x64](https://github.com/rdiankov/openrave/blob/master/docs/Tutorial%20for%20Installing%20Openrave%20in%20Ubuntu-Ubuntu%20Mate%2014.04.2%20x64.rst)


- Own Experience

Tutorial made by [Delton Ding](mailto:dsh0416@gmail.com)

Last Update 15 March, 2016

## Install Package Dependences

There is no official package manager on OS X, but [Homebrew](http://brew.sh/) is what used for most OS X developers. I strongly recommend you to use this, in order to get the dependences correctly and conveniently on OS X.

In order to build from source code, you also need to Install the XCode Command Line Tools for compiling C++ and making files inside the Terminal. run `xcode-select —install` in your Teminal, it would start a Installer, and you could just follow the instructions.

1. `brew install qt`
2. `brew install cmake`
3. `brew install python`
4. `brew install boost --with-python`
5. `brew install boost-python`

## Install Customized Version of COLLADA-DOM

The Openrave use a customized version of COLLADA-DOM, so that the official binary version for OS X may not fit properly. You'd better build the forked version to ensure the compatibility with Openrave.

1. `git clone https://github.com/rdiankov/collada-dom.git`
2. `mkdir -p build`
3. `cmake ..`
4. `make`
5. `make install`

