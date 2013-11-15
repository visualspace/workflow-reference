.. highlight:: bash

.. _tools:

Tools
=====

Tools used for :ref:`html`, :ref:`css` and :ref:`js` in web development.

Yeoman
------
Yeoman bundles Grunt_ and Bower_ with the scaffolding tool
Yo_ used to setup a new web application
as follows::

    yo webapp

.. seealso::
    * `Yeoman <http://yeoman.io/>`_
    * `Yo <https://github.com/yeoman/yo>`_

Grunt
-----
Grunt is a build tool for compiling static HTML, CSS, JS and the likes from
source files such as SCSS. It can be used to automatically recompile, show
and/or reload files in the browser by running::

    grunt watch

.. seealso:: http://gruntjs.com/

Bower
-----
Bower is used like a package manager for client-side JS, CSS and other
packages. It automatically installs, updates and manages libraries such
as :ref:`bootstrap`. For example, installing :ref:`backbone` is easy::

    bower install backbone

This will also include Backbone dependencies such as :ref:`underscore`.

.. seealso:: http://bower.io/


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
but a port using :ref:`Compass` is available as `Sass Bootstrap`_.

.. _templates: http://getbootstrap.com/getting-started/#template
.. _examples: http://getbootstrap.com/getting-started/#examples
.. _CSS: http://getbootstrap.com/css/
.. _reusable components: http://getbootstrap.com/components/
.. _jQuery plugins: http://getbootstrap.com/javascript/

.. seealso::
    * `Bootstrap's website <http://getbootstrap.com/>`_
    * `Sass Bootstrap <http://alademann.github.io/sass-bootstrap/>`_

Cross-browser testing
---------------------
It is essential to test the design and functioning of a site across a range of
different browsers and devices. To make this simpler, several services exist
to create screenshots of webapps in different browser environments and/or to
have live access to apps on different browsers and devices.


.. seealso::
    * `BrowserStack <http://www.browserstack.com/>`_
    * `SauceLabs <https://saucelabs.com/>`_
