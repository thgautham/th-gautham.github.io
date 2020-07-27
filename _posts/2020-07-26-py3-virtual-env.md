---
title: "Installing packages using pip and virtual environments"
date: 2020-07-26
tags: []
header:
  image: "/images/mountain-image-3.jpg"
  caption: "Photo credit: [**Unsplash.com**](https://unsplash.com)"
excerpt: "Scratchpad on how to install packages using pip and virtual
environment manager."
---
### Installing pip
_pip_ is the reference Python package manager. 
On windows, access pip using:

`
py -m pip --version
`

Make sure that the pip is up-to date by running:

`
py -m pip install --upgrade pip
`
---
### Installing virutalenv

_virtualenv_ is used to manage Python packages for different projects.
Install virtualenv using pip.

`py -m pip install --user virtualenv
`
---
### Activating a virtual environment

Activating a virutal environment will put the virtual environment-specific
python and pip executables into your shell's `PATH`.<br/>
On Windows:<br/>
`.\env\Scripts\activate`
Confirm we're in the virtual environment by checking the location of
our Python interpreter, it should point to the `env` directory.<br/>
`where python`<br/>
---
### Leaving the virtual environment
If we want to switch projects or start a new `env` then run:<br/>
`deactivate`
---
### Installing packages
In the virtual environment, we can install our packages, 
- Lets install the _Requests_ library from the Python packaged index (PyPI)<br/>
`pip install requests`
---
### Installing from version control systems(VCS)
`pip` can install packages directly from their version control system:<br/>

<figure>
    <a href="/images/vcs-help.jpg"><img src="/images/vcs-help.jpg"></a>
    <figcaption>example repository layout</figcaption>
</figure>
