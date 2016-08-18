# Installation

The instructions to install IJavascript are platform-dependent and very much
determined by the following dependencies:

- [ZeroMQ](http://zeromq.org/)
- [Node.js](http://nodejs.org/)
- [npm](https://www.npmjs.com/)
- [Jupyter notebook](http://jupyter.org/)

## Debian and Ubuntu

The Jupyter notebook is not yet available in the Debian 8.3 and Ubuntu 16.04 LTS
repositories. Instead, the IPython notebook can be installed:

```sh
sudo apt-get install nodejs-legacy npm ipython ipython-notebook libzmq3-dev
```

Alternatively, the Jupyter notebook can be installed via `pip` or `Anaconda`.

`pip` installs the latest Jupyter release from the [Python Package
Index](https://pypi.python.org/pypi):

```sh
sudo apt-get install nodejs-legacy npm g++ libzmq3-dev python-dev python-pip
sudo pip install --upgrade jupyter
```

And [Anaconda](http://continuum.io/downloads) provides data science platform
that distributes both `Jupyter` (by default) and `Node.js` (optionally).
IJavascript can be installed in an Anaconda setup as follows:

```sh
conda install nodejs
sudo apt-get install libzmq3-dev
sudo npm install -g ijavascript
```

### Global installation

IJavascript can be installed globally (i.e. for all users in the system) by
running:

```sh
sudo npm install -g ijavascript
```

### Local installation

It is also possible to install IJavascript locally, by setting the `npm` prefix
to your home folder:

```sh
npm config set prefix ~
npm install -g ijavascript
```

Note that the above command will install the executable `ijs` in the folder
`~/bin/` and the ijavascript package in `~/lib/node_modules`.

### PPA repository

Gordon Ball has set up a [PPA
repository](https://launchpad.net/%7Echronitis/+archive/ubuntu/jupyter) that
builds deb packages for IJavascript and other Jupyter kernels:

```sh
sudo add-apt-repository ppa:chronitis/jupyter
sudo apt update
sudo apt install ijavascript
```

### Older versions of Debian and Ubuntu

To install IJavascript in older versions of Debian and Ubuntu, `Node.js` needs
upgrading to a recent version. You can do so by running:

```sh
sudo apt-get install curl
curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
sudo apt-get install -y nodejs
```

The instructions for upgrading `Node.js` have been adapted from those found
[here](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions).

## OS X

The below instructions to install the dependencies of IJavascript in OS X make
use of [Homebrew](http://brew.sh/) and [pip](https://pip.pypa.io/):

```sh
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install pkg-config node zeromq
sudo easy_install pip
sudo pip install --upgrade pyzmq jupyter
```

Once the dependencies have been installed, `npm` can be used to install
IJavascript as described above in the section for Ubuntu and Debian.

Also note that the build tool `node-gyp` (which is part of Node.js and is used
to compile native modules) requires Python 2.

## Windows

`Jupyter` could be installed following the instructions
[here](http://jupyter.readthedocs.org/en/latest/install.html). I find more
convenient to install a Python distribution such as
[Anaconda](http://continuum.io/downloads). `Anaconda` not only installs
`Jupyter` and its requirements, but also a selection of frequently-used Python
packages.

`Node.js` provides a [Windows installer](https://nodejs.org/download/). However,
the build tool `node-gyp` will not be functional unless one of the recognised
C++ compilers is installed. See [here](https://github.com/TooTallNate/node-gyp)
for more details,
[here](http://www.microsoft.com/en-us/download/details.aspx?id=34673) for Visual
Studio Express 2012 or
[here](https://www.visualstudio.com/products/visual-studio-express-vs) for a
link to Visual Studio Express 2013.

## Other platforms

For other platforms, instructions to install the IJavascript dependencies may be
found at:
- http://nodejs.org/download/
- http://jupyter.readthedocs.org/en/latest/install.html
- http://zeromq.org/intro:get-the-software
