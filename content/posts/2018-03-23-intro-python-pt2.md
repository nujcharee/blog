---
title: Introducing Python for data scientists - Pt2
author: Leo
date: '2018-03-23'
categories:
  - Python
  - Data Science
tags:
  - Data Science
  - Python
  - Anaconda
  - Fundamentals 
---


This second part of the 'Python for Data Scientists' post talks about
the specifics of Python for data scientists. Part 1 of Python for Data
Scientists talks about Python generally and can be found
[here](https://itsalocke.com/blog/introducing-python-for-data-scientists---pt1/).

Python for data scientists
==========================

Where you can use Python
------------------------

Python is a general purpose programming language meaning that is has
many use cases outside of data science. These include game development, graphics,
web development, GIS, and control systems. A benefit of
this is that data analytics undertaken with Python can easily be
integrated with other tools. Python is an easy language to learn and the
capability of Python for advanced analytics is quickly growing. Here's a
data visualisation video that uses Python:

{{< vimeo 121462010 >}}

Key packages for data science
-----------------------------

The packages mentioned in [Part 1](https://itsalocke.com/blog/introducing-python-for-data-scientists---pt1/) are all used
extensively for data science. Additional useful packages are:

-   [Matplotlib](https://matplotlib.org/) - data visualizations
-   [ggplot](http://ggplot.yhathq.com/) - graphical plotting based on
    R's ggplot2
-   [Seaborn](https://seaborn.pydata.org/) - statistical model
    visualizations
-   [Bokeh](https://bokeh.pydata.org/en/latest/) - interactive
    visualizations
-   [Plotly](https://plot.ly/python/) - Web based toolbox for web
    visualizations
-   [SciKit-Learn](http://scikit-learn.org) - machine learning and image
    processing
-   [Theano](http://deeplearning.net/software/theano/) - machine
    learning framework
-   [Keras](https://keras.io/) - high-level neural networks
-   [NLTK](https://www.nltk.org/) - Natural Language processing
-   [Scrapy](https://scrapy.org/) - web crawling framework
-   [Statsmodels](https://www.statsmodels.org/stable/index.html) -
    estimation of statistical models and conducting statistical tests
    and data exploration

Important things to learn
-------------------------

Learning to use the previously mentioned packages is essential for using
Python for data science.

Python is a dynamically-typed language, this means that a user does not need to define what 'type' a variable is (e.g. numbers or text) when they create a new variable; this is in contrast to statically-typed languages such as Java. A dynamically-typed language is generally less verbose meaning it can be written, read and maintained in a shorter time frame. However errors can be created if Python assigns variables as the wrong 'type' and the user does not check this. In addition  type errors are not checked at the start of execution (as they are for statically-typed languages) and so type errors in large programs are only found after wasting time running the first half of the code. 

Iteration is an important feature in Python which contrasts to
vectorisation in R (if you come from a R background). For example if you want to add the elements of two lists in Python together, you need to loop through the elements of each list and individually add them (iteration). In R you can simply add the two lists together using one line of code. The Python package NumPy supports vectorisation.  The fundamental idea behind vectorisation is that operations apply at once to an entire set of values. 

Using Python with virtual environments is another key concept to learn
about. The main idea here is that the way that Python packages are
stored on your computer can cause problems when working on multiple
projects. A way to get around these problems is to use virtual
environments. More information on this can be found
[here](https://docs.python.org/3/tutorial/venv.html) and
[here](https://realpython.com/blog/python/python-virtual-environments-a-primer/)

Learning resources
------------------

-   [Python Data Science
    Handbook](https://notebooks.azure.com/jakevdp/libraries/PythonDataScienceHandbook) -
    this is one of the most popular books on Python for data science  
-   [Data
    Camp](https://www.datacamp.com/courses/intro-to-python-for-data-science) -
    provides a free Python for Data Science introductory course
-   [Kaggle](https://www.kaggle.com/) - join a high profile data science
    community, learn new skills and take part in competitions
-   [Pivigo](https://www.pivigo.com/data_scientists.html) - a data
    science community to learn new skills and network
-   [Python Regular
    Expressions](https://developers.google.com/edu/python/regular-expressions) -
    regular expressions are very useful for data cleansing
    