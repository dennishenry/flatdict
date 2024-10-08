FlatDict
========

|Version| |Status| |Coverage| |License|

``FlatDict`` and ``FlatterDict`` are a dict classes that allows for single level,
delimited key/value pair mapping of nested dictionaries. You can interact with
``FlatDict`` and ``FlatterDict`` like a normal dictionary and access child
dictionaries as you normally would or with the composite key.

*For example:*

.. code-block:: python

    value = flatdict2.FlatDict({'foo': {'bar': 'baz', 'qux': 'corge'}})

*would be the same as:*

.. code-block:: python

    value == {'foo:bar': 'baz', 'foo:qux': 'corge'}

*values can be accessed as:*

.. code-block:: python

    print(foo['foo:bar'])

    # or

    print(foo['foo']['bar'])

Additionally, lists and tuples are also converted into dicts using ``enumerate()``,
using the ``FlatterDict`` class.

*For example:*

.. code-block:: python

    value = flatdict2.FlatterDict({'list': ['a', 'b', 'c']})

*will be the same as:*

.. code-block:: python

    value == {'list:0': 'a', 'list:1': 'b', 'list:2': 'c'}

API
---

Documentation is available at https://flatdict.readthedocs.io

Versioning
----------
This package attempts to use semantic versioning. API changes are indicated
by the major version, non-breaking improvements by the minor, and bug fixes
in the revision.

It is recommended that you pin your targets to greater or equal to the current
version and less than the next major version.

Installation
------------

.. code-block:: bash

    $ pip install flatdict2

Note that as of 4.0, setuptools 39.2 or higher is required for installation.

.. |Version| image:: https://img.shields.io/pypi/v/flatdict2.svg?
   :target: https://pypi.python.org/pypi/flatdict2

.. |Status| image:: https://github.com/dennishenry/flatdict2/workflows/Testing/badge.svg
   :target: https://github.com/dennishenry/flatdict2/actions
   :alt: Build Status

.. |Coverage| image:: https://img.shields.io/codecov/c/github/dennishenry/flatdict2.svg?
   :target: https://codecov.io/github/dennishenry/flatdict2?branch=main

.. |License| image:: https://img.shields.io/pypi/l/flatdict2.svg?
   :target: https://flatdict.readthedocs.org
