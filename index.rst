.. Intro to Python documentation master file, created by
   sphinx-quickstart on Sun Apr 22 09:58:05 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Sponsors
========

.. image:: images/sponsors.jpg

Intro to Python
===============

Andrew Schoen | @andrewschoen | @pythonkc

.. include:: _templates/pykc-logo.rst

Python
------

Python has a culture which finds an ideal balance between fast-moving innovation and diligent caution. It emphasizes readability, minimizes "magic," treats documentation as a first-class concern, [...] It blends approachability for beginners with maintainability for large projects, which has enabled its presence in fields as diverse as scientific computing, video games, systems automation, and the web.

Source: `Heroku - Python and Django`_

.. _Heroku - Python and Django: http://blog.heroku.com/archives/2011/9/28/python_and_django/

.. include:: _templates/pykc-logo.rst

Python
------

dynamic and strongly typed

interpreted

whitespace is significant

multi-paradigm (OO, impertative, functional)

everything is an object

.. include:: _templates/pykc-logo.rst

Python
------

Created by Guido van Rossum in 1991

Is very diverse in it's usuage.  Science, gaming, web and systems automation.

Has a very clearly-stated list of values

Development is driven through the use of PEPs (Python Enhancement Proposals)

.. include:: _templates/pykc-logo.rst

python -c "import this"
=======================

The Zen of Python, by Tim Peters

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
    >>> a, b, c = y
    >>> a
    1
    >>> b
    2
    >>> a = b = c = 1
    >>> a, b, c
    (1, 1, 1)

.. include:: _templates/pykc-logo.rst


Strings
-------

::

    $ python
    >>> foo = "hello"
    >>> bar = "world"
    >>> "%s %s!!" % (foo, bar)
    'hello world!!'
    >>> foo + " " + bar
    'hello world!!'
    >>> "The answer is %d" % 42
    'The answer is 42'
    >>> ",".join((foo, bar))
    'hello,world'
    >>>>>> ",".join((foo, bar)).split(',')
    ['hello', 'world']

.. include:: _templates/pykc-logo.rst

Functions
---------

::

    $ python
    >>> def add(x, y):
    ...     return x + y
    ... 
    >>> add(2, 4)
     6
    >>> foo = (4, 6, add)
    >>> foo[2](foo[0], foo[1])
    10
    >>> def bar(greeting, bangs=4):
    ...     print "%s%s" % (greeting, "!" * bangs)
    ... 
    >>> bar("hello world", bangs=6)
    hello world!!!!!!

.. include:: _templates/pykc-logo.rst

Functions
---------

::

    $ python
    >>> def foo(*args, **kwargs):
    ...     for arg in args:
    ...         print arg
    ...     for k, v in kwargs.iteritems():
    ...         print "%s=%s" % (k, v)
    ... 
    >>> foo("1", "2", key="value")
    1
    2
    key=value

.. include:: _templates/pykc-logo.rst

Functions
---------

::

    $ python
    >>> def foo(name):
    ...     def bar():
    ...         return "Hello from %s" % name
    ...     print bar()
    ... 
    >>> foo('Andrew')
    Hello from Andrew

.. include:: _templates/pykc-logo.rst

Functions
---------

::

    $ python
    >>> def f(x):
    ...     return x*2
    ...
    >>> f(3)
    6
    >>> times_two = lambda x: x*2
    >>> times_two(3)
    6
    >>> (lambda x: x*2)(3)
    6

.. include:: _templates/pykc-logo.rst

Classes
-------

::

    $ python
    >>> class Person(object):
    ...     def __init__(self, name="Andrew"):
    ...         self.name = name
    ...     def my_name(self):
    ...         print "My name is %s" % self.name
    ... 
    >>> kid = Person(name="Anderson")
    >>> kid.my_name()
    My name is Anderson
    >>> me = Person()
    >>> me.my_name()
    My name is Andrew

.. include:: _templates/pykc-logo.rst

Classes
-------

::

    $ python
    >>> class Bar(object):
    ...     def from_bar(self):
    ...         print "from bar"
    >>> class Baz(object):
    ...     def from_baz(self):
    ...         print "from baz"
    >>> class Foo(Bar, Baz):
    ...     def from_baz(self):
    ...         print "overloaded!"
    >>> x = Foo()
    >>> x.from_bar()
    from bar
    >>> x.from_baz()
    overloaded!

.. include:: _templates/pykc-logo.rst

Control Structures
==================

.. include:: _templates/pykc-logo.rst

if
--

::

    $ python
    >>> if True:
    ...     print "of course it is true"
    ... 
    of course it is true
    >>> phrase = "hello world"
    >>> if "world" in phrase:
    ...     print "hi world"
    ... 
    hi world

.. include:: _templates/pykc-logo.rst

if
--

::

    $ python
    >>> phrase = "hello world"
    >>> if not phrase:
    ...    print "no phrase"
    ... elif "hello world!!" == phrase:
    ...    print "!!!"
    ... else:
    ...    print phrase
    ... 
    hello world

.. include:: _templates/pykc-logo.rst

for
---

::

    $ python
    >>> for x in range(3):
    ...     print x * 2
    ... 
    0
    2
    4
    >>> opposites = {"up":"down","left":"right"}
    >>> for k, v in opposites.items():
    ...     print "The opposite of %s is %s" % (k, v)
    ... 
    The opposite of up is down
    The opposite of left is right

.. include:: _templates/pykc-logo.rst

for
---

::

    $ python
    >>> abcs = "abc"
    >>> for index, char in enumerate(abcs):
    ...     print index, char
    ... 
    0 a
    1 b
    2 c
    >>> for char in abcs:
    ...     print char
    ... 
    a
    b
    c

.. include:: _templates/pykc-logo.rst

for
---

::

    $ python
    >>> abcs = "abc"
    >>> for char in abcs:
    ...     if "b" in char:
    ...         continue
    ...     print char
    ... 
    a
    c
    >>> for char in abcs:
    ...     if "b" in char:
    ...         break
    ...     print char
    ... 
    a

.. include:: _templates/pykc-logo.rst

Generators
----------

::

    $ python
    >>> def reverse(data):
    ...     for index in range(len(data)-1, -1, -1):
    ...         yield data[index]
    ... 
    >>> reverse('Andy')
    <generator object reverse at 0x1004992d0>
    >>> for char in reverse('Andy'):
    ...     print char
    ... 
    y
    d
    n
    A
    >>> nums = (i*i for i in range(10))
    >>> sum(nums)  # sum of squares
    285

.. include:: _templates/pykc-logo.rst

while
-----

::

    $ python
    >>> i = 0
    >>> while i < 4:
    ...     print i
    ...     i += 1
    ... 
    0
    1
    2
    3

.. include:: _templates/pykc-logo.rst

Exception Handling
------------------

::

    $ python
    >>> def divide(x, y):
    ...     try:
    ...         result = x / y
    ...     except ZeroDivisionError, e:
    ...         print "division by zero"
    ...     else:
    ...         print "result is %d" % result
    ...     finally:
    ...         print "should always print"
    ... 
    >>> divide(2, 1)
    result is 2
    should always print
    >>> divide(2, 0)
    division by zero
    should always print

.. include:: _templates/pykc-logo.rst

Exception Handling
------------------

::

    $ python
    >>> try:
    ...     raise NameError("hello world")
    ... except NameError:
    ...     print 'Got a NameError'
    ...     raise
    ... 
    Got a NameError
    Traceback (most recent call last):
      File "<stdin>", line 2, in <module>
    NameError: hello world

.. include:: _templates/pykc-logo.rst

Built-ins
=========

.. include:: _templates/pykc-logo.rst

Built-ins
---------

::

    $ python
    >>> x = [True, True, False]
    >>> any(x)
    True
    >>> all(x)
    False
    >>> dir(x)
    ['__add__', '__class__', '__contains__', '__delattr__', '__delitem__',
     '__delslice__', '__doc__', '__eq__', '__format__', '__ge__', 
     '__getattribute__', '__getitem__', '__getslice__', '__gt__', '__hash__',
      '__iadd__', '__imul__', '__init__', '__iter__', '__le__', '__len__',
       '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', 
       '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', 
       '__setattr__', '__setitem__', '__setslice__', '__sizeof__', '__str__', 
       '__subclasshook__', 'append', 'count', 'extend', 'index', 'insert', 
       'pop', 'remove', 'reverse', 'sort']

.. include:: _templates/pykc-logo.rst

Built-ins
---------

::

    $ python
    >>> x = "100"
    >>> int(x)
    100
    >>> y = 100
    >>> str(y)
    '100'
    >>> len(x)
    3
    >>> type(y)
    <type 'int'>

.. include:: _templates/pykc-logo.rst

Built-ins
---------

::

    $ python
    >>> nums = [1, 2, 3, 4]
    >>> map(lambda x: x*2, nums)
    [2, 4, 6, 8]
    >>> abcs = ['a','b','c','d']
    >>> zip(nums, abcs)
    [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]
    >>> filter(lambda x: x % 2 == 0, nums)
    [2, 4]
    >>> max(nums)
    4
    >>> min(nums)
    1

.. include:: _templates/pykc-logo.rst

Built-ins
---------

::

    $ python
    >>> class Person(object):
    ...     def __init__(self, name="Andrew"):
    ...             self.name=name
    ...     def my_name(self):
    ...             print "My name is %s" % self.name
    ... 
    >>> me = Person()
    >>> hasattr(me, 'my_name')
    True
    >>> attr = getattr(me, 'my_name')
    >>> attr
    <bound method Person.my_name of <__main__.Person object at 0x10049cc50>>
    >>> attr() if callable(attr) else attr
    My name is Andrew

.. include:: _templates/pykc-logo.rst

Python Resources
________________

* http://docs.python.org
* http://learnpythonthehardway.org/
* http://diveintopython.net
* http://codingbat.com/python
* http://pythonchallenge.com 

.. include:: _templates/pykc-logo.rst

Python Projects
_______________

If you'd like to learn more about different projects in Python, check these out.  Pip and virtualenv are a must for any Python dev.

* `pip`_
* `virtualenv`_
* `Django`_ 
* `south`_
* `Sphinx`_
* `fabric`_

.. _pip: http://pypi.python.org/pypi/pip
.. _virtualenv: http://pypi.python.org/pypi/virtualenv
.. _Django: https://www.djangoproject.com/
.. _south: http://south.aeracode.org/
.. _Sphinx: http://sphinx.pocoo.org/
.. _fabric: http://docs.fabfile.org/en/1.4.1/index.html

.. include:: _templates/pykc-logo.rst

Beginners Python Workshop
==========================

The Beginners Python Workshop is a 2-day free event focused on teaching the basics of programming in the Python language.  Everybody is encouraged to attend, regardless of your previous experience with programming.

Friday, June 22nd 6pm - 10pm

Saturday, June 23rd 10am - 4pm

UMKC Campus - 302 Flarsheim Hall

.. include:: _templates/pykc-logo.rst

Thanks!
=======

@andrewschoen

@pythonkc

http://www.meetup.com/pythonkc

https://github.com/andrewschoen/intro-to-python

.. include:: _templates/pykc-logo.rst













































