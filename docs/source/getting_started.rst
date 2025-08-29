Getting started
******************

.. _installation:

Installation
------------

To use NanoPolaris, first install it using pip:

.. code-block:: console

   (.venv) $ pip install nanopolaris

Creating recipes
----------------

To retrieve a list of xxx,
you can use the ``xxx.get_xxx()`` function:

.. autofunction:: nanopolaris.get_xxx

The ``xxx`` parameter should be either ``"yyy"``, ``"zzz"``,
or ``"zxy"``. Otherwise, :py:func:`nanopolaris.get_xxx`
will raise an exception.

.. autoexception:: nanopolaris.InvalidKindError

For example:

>>> import nanopolaris
>>> nanopolaris.get_xxx()
['xxx', 'yyy', 'zzz']

