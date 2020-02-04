---
layout: default
title: Translante IDL script to python
category: timeline
tags: article
---

## IDL programming language
IDL, short for Interactive Data Language, is a programming language used for data analysis. It is popular in particular areas of science, such as astronomy, atmospheric physics and medical imaging. (https://en.wikipedia.org/wiki/IDL_(programming_language))

## IDL to python (numpy) document
- (IDL to Numeric/numarray Mapping)[https://www.johnny-lin.com/cdat_tips/tips_array/idl2num.html]
- (NumPy for IDL users)[http://mathesaurus.sourceforge.net/idl-numpy.html]

## idlwrap API
idlwrap helps you port IDL code to python by providing an IDL-like interface to numpy and scipy.
- (API)[https://r4lv.github.io/idlwrap/api.html]

## Note
- Array
  - IDL a[i, *] is the same with Python a[:,i]
    There are two different ways of storing a matrix/array in memory: column-major and row-major. 
  - IDL array index include the last element: 
    ```IDL
    IDL> (FLTARR(10))[3:5]
     0.00000      0.00000      0.00000 ; -> three elements
    ```
    ```
    >>> np.zeros(10)[3:5]
    array([0., 0.]) # -> two elements
    ```