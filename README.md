ipython_notebook_goodies
========================

Random goodies for use in iPython Notebooks. 
Tested with the latest iPython Notebook 3.2.0

1. Table of Contents
--------------------

Make a table of contents for your notebook. Uses headings (e.g. H1, H2, etc.) to build TOC, 
and provides anchors (added where needed).

**Usage FOR JUPYTER NOTEBOOK:** 

1. Add a *markdown* cell at the top of your notebook with the following:
```
<h1 id="tocheading">Table of Contents</h1>
<div id="toc"></div>
```
2. Add a *code* cell anywhere in the notebook with the following:
```
%%javascript
$.getScript('https://kmahelona.github.io/ipython_notebook_goodies/ipython_notebook_toc.js')
```


**Usage FOR JUPYTER LAB:** 

1. Add a *markdown* cell at the top of your notebook with the following:
```
<h1 id="tocheading">Table of Contents</h1>
<div id="toc"></div>
```
2. Add a *code* cell anywhere in the notebook with the following:
```
%%javascript
// this code block is to configure the table of contents to work as intended
    var script = document.createElement('script');
    script.type = 'text/javascript';
    script.src = 'https://code.jquery.com/jquery-3.4.1.min.js';
    document.head.appendChild(script);
    
$.getScript('https://kmahelona.github.io/ipython_notebook_goodies/ipython_notebook_toc.js')
```
This solution for Jupyter Lab was taken from https://github.com/kmahelona/ipython_notebook_goodies/issues/6#issue-462642204

Another important note: if you do not want the title of your notebook to display in the table of contents, give it the tocheading id and format it as
```
<h1 id="tocheading">Page Title</h1>


```
