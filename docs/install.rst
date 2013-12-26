.. _install:

Installation
============

There are several ways to install lilac, but the recommended one is to install lilac
with :ref:`Virtualenv <virtualenv-label>`.

OS Support
----------

Lilac supports only \*nix: Mac OS X, Linux, BSD (Only linux tested).

.. _virtualenv-label:

Virtualenv
----------

If you are a pythoner, you should install lilac via `virtualenv <http://www.virtualenv.org/>`_ .

If virtualenv is not installed on your OS, install it:

.. code-block:: bash

    $ sudo pip install virtualenv

Once you have virtualenv installed, open a shell and create a new environment for your blog:

.. code-block:: bash

    $ mkdir MyBlog
    $ cd MyBlog
    $ virtualenv venv
    New python executable in venv/bin/python
    Installing setuptools............done.
    Installing pip...............done.

Now, whenever you want to write blog, you have to activate the corresponding environment:

.. code-block:: bash

    $ . venv/bin/activate

Then, install lilac in your virtualenv:

.. code-block:: bash

    $ pip install lilac

System-Wide Installation
------------------------

Just run `pip` with root privileges:

.. code-block:: bash

    $ sudo pip install lilac

Get the Code
-------------

Lilac is hosted on GitHub, where you can get `the latest code <https://github.com/hit9/lilac>`_.

You can clone the repository:

.. code-block:: bash

    $ git clone git://github.com/hit9/lilac.git

Or, download the `tarball <https://github.com/hit9/lilac/tarball/master>`_.

Once you get the code, you can install it into your site-packages:

.. code-block:: bash

    $ [sudo] python setup.py install

Upgrade your Lilac
-------------------

Whenever you want to upgrade your lilac to latest version:

.. code-block:: bash

    $ [sudo] pip install lilac --upgrade


You may want to see the :ref:`Quick Start <quickstart>` part now.

Installation trouble?
---------------------

If you meet problems similar to this: ``Cann't find Python.h``, try to install Python development libraries.


If your're using Ubuntu, install it via:

.. code-block:: bash

    $ [sudo] apt-get install python-dev

There's no this issue on OS X.
