> docs.python-guide.org/en/latest

[TOC]

## Modules to use for..

### Testing

#### Test runner

1. nose (popular, autofind)

#### Framework

1. unittest (classic, builtin)
1. py.test

### Documentation

#### Creating

1. Sphinx (new, popular, needs to import all modules)
1. Epydoc (classic, easy, suposedly discontinued)
  1. Or, pyreverse -o png (UML only)
1. doxygen (doxypy, limited)

#### Reading

1. pydoc

### Style/syntax chackers

#### Checker

1. pylint (syntax and style, pyreverse comes with it..)
1. pyflakes (errors), flake8 (for style)

#### Converter

1. autopep8 (style)
1. rope (refactoring)

### Settings

1. ConfigParser (builtin) with .ini
  1. OR just use globals in a global_settings.py

### Interactive

1. Ipython (notebooks, htlm, standard, scipy integration)
1. bpython (inline completion)

### UI Frameworks -- GUIs

1. pyQt (around a while, up to date, need license if not open src) OR pyside (Qt, some call buggy) -- Qt Designer; Eric Python IDE
  - Qt uses signal/slots
1. wxPython (no python 3, late 2014 update, looks uniform) -- gui2py
  - Callbacks
1. tkInter (builtin, slighly uglier, less powerful) -- PAGE
  - Callbacks
1. Kivy (all device/OSs, OpenGL ES2, confusing install) -- Kivy-Designer
1. matplotlib (basic, for math tools)

### Gaming

1. pyGame (2d, lots of support) -- ??
1. pyglet (3d, updated mid 2014) -- ??

### Math/science

1. scipy
  1. matplotlib
  1. numpy
  1. pandas
  1. sympy

### IDEs

1. VIM
2. Spyder (for science)

### Networking app

1. tornado (async, simple repo, websockets)
  1. or asyncore, asynchat, asyncio
  1. or twisted (low level, has state)
1. django (high level, runs http server, syncronous) -- great github repo
1. flask (microframework) -- great github repo
1. requests (http)

### Images/ing

1. Pillow, PIL

### Command line interface

1. Click (vs argparse, etc)

## Making a user package globally accessible

> http://stackoverflow.com/questions/16196268

1. Create ~/.local/lib/pythonX.X/site-packages
1. Soft link file or package here

