.. highlight:: console

.. _tools:

Tools
=====

Tools used for :ref:`html`, :ref:`css` and :ref:`js` in web development.

.. _yeoman:

Yeoman
------
Yeoman bundles Grunt_ and Bower_ with the scaffolding tool
Yo used to setup a new web application
as follows::

    yo webapp

.. seealso::

    Yeoman
        http://yeoman.io/

    Yo
        https://github.com/yeoman/yo


.. _grunt:

Grunt
-----
Grunt is a build tool for compiling static HTML, CSS, JS and the likes from
source files such as SCSS. It can be used to automatically recompile, show
and/or reload files in the browser by running::

    grunt watch

.. seealso::

    Grunt
        http://gruntjs.com/


.. _assemble:

Assemble
--------
Assemble is a static site generator for use with :ref:`grunt`. Starting an
assemble project is easy with :ref:`yeoman`::

    npm install -g generator-assemble
    mkdir project && cd project
    yo assemble

.. seealso::

    Using assemble with Yeoman (adding Yeoman to an existing project)
        http://www.fettblog.eu/blog/2013/09/02/using-assemble-io-with-yeoman-ios-webapp-gruntfile/

    assemble
        http://assemble.io/

    Yeoman assemble generator
        https://github.com/assemble/generator-assemble


Bower
-----
Bower is used like a package manager for client-side JS, CSS and other
packages. It automatically installs, updates and manages libraries such
as :ref:`bootstrap`. For example, installing :ref:`backbone` is easy::

    bower install backbone

This will also include Backbone dependencies such as :ref:`underscore`.

.. seealso::

    Bower
        http://bower.io/


.. _bootstrap:

Twitter's Bootstrap
-------------------
Bootstrap is a comprehensive front-end framework consisting of:

* A basic HTML templates_ and good examples_.
* CSS_ with a grid systemm, sensible defaults for tags and styling
  for UI elements.
* `Reusable components`_ built to provide iconography, dropdowns, navigation,
  alerts, popovers, and much more.
* `jQuery plugins`_ for common interaction patterns.

The original version of bootstrap is built using `Less CSS <http://lesscss.org/>`_
but a port using :ref:`Compass` is available as Sass Bootstrap.

.. _templates: http://getbootstrap.com/getting-started/#template
.. _examples: http://getbootstrap.com/getting-started/#examples
.. _CSS: http://getbootstrap.com/css/
.. _reusable components: http://getbootstrap.com/components/
.. _jQuery plugins: http://getbootstrap.com/javascript/

.. seealso::

    Bootstrap
        http://getbootstrap.com/

    Sass Bootstrap
        http://alademann.github.io/sass-bootstrap/


Cross-browser testing
---------------------
It is essential to test the design and functioning of a site across a range of
different browsers and devices. To make this simpler, several services exist
to create screenshots of webapps in different browser environments and/or to
have live access to apps on different browsers and devices.


.. seealso::

    BrowserStack
        http://www.browserstack.com/

    SauceLabs
        https://saucelabs.com/


.. _polyfills:

Polyfills
---------
Tools allowing new HTML and CSS features to be used in browser that do not (yet) support them.

.. _picturefill:

Picturefill
^^^^^^^^^^^
An adaptive ('retina') images approach that you can use today that mimics the proposed :ref:`picture`.

.. seealso:: https://github.com/scottjehl/picturefill


.. _srcset-polyfill:

srcset-polyfill
^^^^^^^^^^^^^^^

.. seealso:: https://github.com/borismus/srcset-polyfill


