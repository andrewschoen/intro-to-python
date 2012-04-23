.. Intro to Python documentation master file, created by
   sphinx-quickstart on Sun Apr 22 09:58:05 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Intro to Python
===============

Andrew Schoen | @andrewschoen | @pythonkc

.. include:: _templates/pykc-logo.rst

Python
------

Python has a culture which finds an ideal balance between fast-moving innovation and diligent caution. It emphasizes readability, minimizes "magic," treats documentation as a first-class concern, [...] It blends approachability for beginners with maintainability for large projects, [...] scientific computing, video games, systems automation, and the web.

Source: `Heroku - Python and Django`_

.. _Heroku - Python and Django: http://blog.heroku.com/archives/2011/9/28/python_and_django/

.. include:: _templates/pykc-logo.rst

Python
------

dynamic and strongly typed

interpreted

whitespace sensitive

multi-paradigm (OO, impertative, functional)

.. include:: _templates/pykc-logo.rst

Python
------

Created by Guido van Rossum in 1991

Is very diverse in it's usuage.  Science, gaming, web and systems automation.

Has a very clearly-stated list of values

.. include:: _templates/pykc-logo.rst

The Zen of Python
=================

Beautiful is better than ugly.

Explicit is better than implicit.

Simple is better than complex.

Complex is better than complicated.

Flat is better than nested.

Sparse is better than dense.

Readability counts.

Special cases aren't special enough to break the rules.

Although practicality beats purity.

Errors should never pass silently.

Unless explicitly silenced.

.. include:: _templates/pykc-logo.rst

The Zen of Python (cont)
========================

In the face of ambiguity, refuse the temptation to guess.

There should be one-- and preferably only one --obvious way to do it.

Although that way may not be obvious at first unless you're Dutch.

Now is better than never.

Although never is often better than *right* now.

If the implementation is hard to explain, it's a bad idea.

If the implementation is easy to explain, it may be a good idea.

Namespaces are one honking great idea -- let's do more of those!

.. include:: _templates/pykc-logo.rst

Python Syntax & Datatypes
=========================

.. include:: _templates/pykc-logo.rst

Lists
-----

::
    
    $ python
    >>> x = ['one', 'two', 'three']
    >>> x.append(4)
    >>> x
    ['one', 'two', 'three', 4]
    >>> x.remove('one')
    >>> x
    ['two', 'three', 4]
    >>> x.pop(1)
    'three'
    >>> x
    ['two', 4]
    >>> x.insert(0, "one")
    ['one', 'two', 4]

.. include:: _templates/pykc-logo.rst

Lists
-----

::

    $ python
    >>> x = ['one', 'two', 'three', 4]
    >>> x[1]
    'two'
    >>> x[0:2]
    ['one', 'two']
    >>> x[:-1]
    ['one', 'two', 'three']
    >>> x[-1]
    4
    >>> x[0::2]
    ['one', 'three']

.. include:: _templates/pykc-logo.rst

List Comprehensions
-------------------

::

    $ python
    >>> nums = [1, 2, 3, 4]
    >>> [x * 2 for x in nums]
    [2, 4, 6, 8]
    >>> [x for x in nums if x % 2 == 0]
    [2, 4]

.. include:: _templates/pykc-logo.rst

List Comprehensions
===================

::

    $ python
    >>> s = 'string-with-palindromes-like-abbalabba'
    >>> l = len(s)
    >>> [s[x:y] for x in range(l) for y in range(x,l+1) if p(s[x:y])] 
    wat

.. image:: images/wat-3.jpeg
.. image:: images/wat-1.jpeg
.. image:: images/wat-2.jpeg

Powerful, but watch out for readability. 

**Readability counts & Simple is better than complex**

.. include:: _templates/pykc-logo.rst

Dictionaries
------------

::

    $ python
    >>> x = {}
    >>> x
    {}
    >>> x = dict()
    >>> x
    {}
    >>> x = {'hello':'world'}
    >>> x
    {'hello': 'world'}

.. include:: _templates/pykc-logo.rst

Dictionaries
------------

::

    $ python
    >>> opposites = {'up':'down', 'left':'right'}
    >>> opposites
    {'up': 'down', 'left': 'right'}
    >>> opposites['hot'] = 'cold'
    >>> oposites
    {'hot': 'cold', 'up': 'down', 'left': 'right'}
    >>> del opposites['up']
    >>> opposites
    {'tall': 'short', 'hot': 'cold', 'left': 'right'}
    >>> opposites['tall']
    'short'

.. include:: _templates/pykc-logo.rst

Dictionaries
------------

::

    $ python
    >>> opposites = {"up":"down", "left":"right"}
    >>> opposites['dark']
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    KeyError: 'dark'
    >>> opposites.get('dark', 'light')
    'light'

.. include:: _templates/pykc-logo.rst

Dictionaries
------------

::

    $ python
    >>> opposites = {"up":"down", "left":"right"}
    >>> opposites.keys()
    ['up', 'left']
    >>> opposites.values()
    ['down', 'right']
    >>> ["The opposite of %s is %s" % (k, v) for 
             k, v in opposites.iteritems()]
    ['The opposite of up is down', 'The opposite of left is right']

.. include:: _templates/pykc-logo.rst

Tuples
------

::

    $ python
    >>> nums = (1, 2, 3)
    >>> abcs = ('a', 'b', 'c')
    >>> nums[1]
    2
    >>> # tuples can be nested
    ... nested = ('x', 'y', 'z'), nums, abcs
    >>> nested
    (('x', 'y', 'z'), (1, 2, 3), ('a', 'b', 'c'))

.. include:: _templates/pykc-logo.rst

Tuples
------

::

    $ python
    >>> foo = (1, 2)
    >>> foo[0] = 3
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: 'tuple' object does not support item assignment

Tuples are immutable

.. include:: _templates/pykc-logo.rst

Variables
---------

::

    $ python
    >>> x
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'x' is not defined
    >>> x = 1
    >>> x
    1
    >>> y = (1, 2, 3)
    >>> (a, b, c) = y
    >>> a
    1
    >>> b
    2
    >>> c
    3

.. include:: _templates/pykc-logo.rst

























