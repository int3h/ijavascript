<nav style="float: left;
            padding: 2em;
            margin: 0 2em 2em 0;
            border: 1px solid;
            border-radius: 10px;
            text-align: center;">
<h1><img alt="Links" src="images/logo-128x128.png"></h1>
<a href="http://n-riesco.github.io/ijavascript">IJavascript Home Page</a><br>
<a href="http://github.com/n-riesco/ijavascript">IJavascript Repository</a><br>
<a href="http://github.com/n-riesco/jp-babel">jp-babel Repository</a><br>
<a href="http://github.com/n-riesco/jp-coffeescript">jp-coffeescript Repository</a><br>
</nav>

# IJavascript

IJavascript is an [`npm` package](https://www.npmjs.com/) that implements a
Javascript kernel for the [Jupyter notebook](http://jupyter.org/) . A Jupyter
notebook combines the creation of rich-text documents (including equations,
graphs and videos) with the execution of code in a number of programming
languages.

The execution of code is carried out by means of a kernel that implements the
[Jupyter messaging
protocol](http://jupyter-client.readthedocs.io/en/latest/messaging.html).
There are kernels available for
[Python](http://ipython.readthedocs.io/en/stable/install/kernel_install.html),
[Babel](https://github.com/n-riesco/jp-babel),
[CoffeeScript](https://github.com/n-riesco/jp-coffeescript),
[Julia](https://github.com/JuliaLang/IJulia.jl),
[Haskell](https://github.com/gibiansky/IHaskell),
[Ruby](https://github.com/minad/iruby) and [many other
languages](https://github.com/ipython/ipython/wiki/IPython-kernels-for-other-languages).

<div style="clear: both;" />

## Announcements

- Starting with IJavascript v5.0.11, it is possible to customise the output of
  an object based on its class. See the documentation on [custom
  output](http://n-riesco.github.io/ijavascript/doc/custom.ipynb.html) for
  details.
- The use of `$$mimer$$` and `$$defaultMimer$$` to customise output is now
  deprecated.
- To avoid clutter in the global context, the use of `$$async$$`, `$$done$$`,
  `$$mime$$`, `$$html$$`, `$$svg$$`, `$$png$$` and `$$jpeg$$` has also been
  deprecated.

## Main Features

- Run Javascript code in a `Node.js` session
- [Hello, World!](http://n-riesco.github.io/ijavascript/doc/hello.ipynb.html)
- [Asynchronous
  output](http://n-riesco.github.io/ijavascript/doc/async.ipynb.html)
- [Custom output](http://n-riesco.github.io/ijavascript/doc/custom.ipynb.html)
- [Autocompletion](http://n-riesco.github.io/ijavascript/doc/complete.md.html):
  press `TAB` to complete keywords and object properties
- [Object
  inspection](http://n-riesco.github.io/ijavascript/doc/inspect.md.html): press
  `Shift-TAB` to inspect an object and show its content or, if available, its
  documentation

## Installation

The instructions to install IJavascript are platform-dependent. For example, in
Ubuntu 16.04, IJavascript and its prerequisites can be installed simply by
running:

```sh
sudo apt-get install nodejs-legacy npm ipython ipython-notebook libzmq3-dev
sudo npm install -g ijavascript
```

In OS X, [Homebrew](http://brew.sh/) and [pip]() can be used to install
IJavascript and its prerequisites:

```sh
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install pkg-config node zeromq
sudo easy_install pip
sudo pip install --upgrade pyzmq jupyter
sudo npm install -g ijavascript
```

In Windows, [Anaconda](http://continuum.io/downloads) offers a convenient
distribution to install Python and many other packages, such as Jupyter and
IJavascript.

For other platforms or if you find any problems with the instructions above,
please, refer to the [installation
notes](http://n-riesco.github.io/ijavascript/doc/install.md.html).

## Usage

To create a Jupyter notebook that runs a session in the IJavascript kernel,
run:

```sh
ijs
```

This command should open the Jupyter dashboard in your default web browser:

![Screenshot: Jupyter Dashboard](images/screenshot-dashboard-home.png)

Here's a sample notebook that makes use of the IJavascript kernel:

![Screenshot: Notebook Hello Sample](images/screenshot-notebook-hello.png)

Please, refer to the [usage
notes](http://n-riesco.github.io/ijavascript/doc/usage.md.html) for further
details.

# Contributions

First of all, thank you for taking the time to contribute. Please, read
[CONTRIBUTING](http://n-riesco.github.io/ijavascript/contributing.html) and use
the [issue tracker](https://github.com/n-riesco/ijavascript/issues) for any
contributions: support requests, bug reports, enhancement requests, pull
requests, submission of tutorials...

# TO DO

- Split kernel into Jupyter and Javascript frameworks to help reuse code in the
  [Babel](https://github.com/n-riesco/jp-babel) and
  [CoffeeScript](https://github.com/n-riesco/jp-coffeescript) kernels.
- Use Mocha test framework
- Complete the implementation of the Jupyter messaging protocol v4.1
- Complete the implementation of the Jupyter messaging protocol v5.0

See the TODO list in the [NEL](https://github.com/n-riesco/nel) package for
additional items.
