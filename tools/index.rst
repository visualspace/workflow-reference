.. highlight:: bash

.. _tools:

Tools
=====

Tools used for :ref:`html`, :ref:`css` and :ref:`js` in web development.

.. _yeoman:

Yeoman
------
Yeoman_ bundles :ref:`grunt` and :ref:`bower` with the scaffolding
tool Yo_ used to setup a new web application as follows::

    yo webapp

.. _grunt:

Grunt
-----
Grunt_ is a build tool for compiling static HTML, CSS, JS and the likes from
source files such as SCSS. It can be used to automatically recompile, show
and/or reload files in the browser by running::

    grunt watch

.. _bower:

Bower
-----
Bower_ is used like a package manager for client-side JS, CSS and other
packages. It automatically installs, updates and manages libraries such
as :ref:`bootstrap`. For example, installing :ref:`backbone` is easy::

    bower install backbone

This will also include Backbone dependencies such as :ref:`underscore`.

.. _bootstrap:

Twitter's Bootstrap
-------------------

.. Yeoman http://yeoman.io/
.. Yo https://github.com/yeoman/yo
.. Grunt http://gruntjs.com/
.. Bower http://bower.io/
