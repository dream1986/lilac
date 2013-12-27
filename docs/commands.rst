.. _commands:

Commands
========

You're going to see how simple its command line interface is.

Overview
--------

All command line usage::

    Usage:
      lilac serve [<port>] [--watch]
      lilac (deploy|build|clean)
      lilac (start|stop|status|restart)
      lilac [-h|-v]
    
    Options:
      -h --help     show this help message
      -v --version  show version
      --watch       watch source files for changes
      <port>        which port for server to use(default: 8888)
    
    Commands:
      deploy        deploy blog in current directory
      build         build source files to htmls
      clean         remove files built by lilac
      serve         start a web server, as a option, start watching
      start         start http server and auto rebuilding as a daemon running in the background
      stop          stop the http server and auto rebuilding daemon
      restart       restart http server and auto rebuilding daemon
      status        report the status of the daemon
    

Options
-------

Show help::

    $ lilac --help

Show version::

    $ lilac --version

Depoly
------

To deploy a new blog in a new-created directory::

    ~/myblog/ $ lilac deploy

Build
-----

To build site from source to htmls, lilac will always be honest to `config.toml`::

    $ lilac build

Clean
-----

To remove all htmls(include the feed.atom) lilac built::

    $ lilac clean

This command is equivalent to:

.. code-block:: bash

    $ rm -rf post page tag 404.html about.html archives.html feed.atom index.html tags.html

.. _command_serve:

Serve
-----

To start a simple HTTP server::

    $ lilac serve

You can tell lilac which port to use(the default port is 8888)::

    $ lilac serve 8080

To watch source changes the same time when the cute web server running::

    $ lilac serve --watch

When you save your writings, lilac can detect the changes and start rebuilding.

**Note**: the preview server will run the site from root ``""`` regardless of the configuration item ``root_path``.

Daemon
------

To start lilac's http server and file monitor as a daemon running in the
background, it will serve the blog at ``0.0.0.0:8888`` and start auto rebuilding once
source files changed::

    $ lilac start

To stop it::

    $ lilac stop

To get its status::

    $ lilac status

To restart it::

    $ lilac restart

.. _ililac:

ililac
------

ililac was removed in version 0.3.9, use ``lilac start|stop|restart|status|`` instead.
