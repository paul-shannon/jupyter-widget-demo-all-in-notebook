# A Simple Jupyter Widget: interactive d3 circle drawing, all code in the notebook

Wishing to become proficient at creating interactive widgets for Jupyter notebooks and labs,
I started out by studying the documentation offered by the jupyter/ipywidgets project:

  -  https://github.com/ipython/ipywidgets   (the project's README is helpful)
  -  http://ipywidgets.readthedocs.io/en/latest/examples/Widget%20Custom.html (provides well-documented incremental examples)

Next, as suggested by those docs, I looked at three more advanced examples.  The ipywidgets README says:

<hr>
Examples of custom widget libraries built upon ipywidgets are

- [bqplot](https://github.com/bloomberg/bqplot) a 2d data visualization library
  enabling custom user interactions.
- [pythreejs](https://github.com/jovyan/pythreejs) a Jupyter - Three.js wrapper,
  bringing Three.js to the notebook.
- [ipyleaflet](https://github.com/ellisonbg/ipyleaflet) a leaflet widget for Jupyter.

<hr>

However, I found these to be rather large and (for me) confusing. They
are big, rich widgets, worth emulating, very useful in themselves, but perhaps not the easiest examples for a
novice widget programmer to learn from:

  - ipyleaflet:  500 lines of python, 800 lines of javascript
  - pqplot: 4300 lines of python, 15000 lines of javascript
  - pythree: 800 lines of python, 2000 lines of javascript

So, with advice from the jupyter-js-widget development team, I embarked upon
an intermediate widget which makes very simple use of the [d3](https://d3js.org/)
interactive graphics library to draw circles on a small widget canvas.  Circles draing
can be initiated from a python cell, or by clicking on the d3 canvas.  I present that widget here 
in one notebook, all self-contained: 16 lines of python and 92 lines of Javascript.  No
auxialliary code or tools required.  

The notebook demonstrates the features of widget programming I most wanted to understand whenI started out: the
logic and structure of a Javascript backbonejs subclass, the complementary python programming idioms
needed to make it work, how to include a public javascript library (in this case, d3).

Juypter widgets are often packaged up into a notebook extensions, then downloaded and installed in a notebook
server.  The same widget presented here is also avaialable as an extension [here](https://github.com/paul-shannon/jupyter-widget-demo-nbextension).
