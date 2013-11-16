.. highlight:: js

.. index::
    ! JavaScript
    see: JS; JavaScript

.. _js:

JavaScript
==========

.. index::
    Asynchronous Module Definition
    see: AMD; Asynchronous Module Definition

.. _amd:

Asynchronous Module Definition
------------------------------
Asynchronous module definition (AMD) is an API for modular JavaScript
development such that defined modules can be loaded asynchronously while
automatically taking care of loading dependencies.

It is useful in improving the performance of websites by bypassing synchronous
loading of modules along with the rest of the site content. In addition to
loading multiple JavaScript files at runtime, AMD can be used during development
to keep JavaScript files encapsulated in many different files.

Defining a module definition in AMD looks as follows::

    define(function (require) {
        var dependency1 = require('dependency1'),
            dependency2 = require('dependency2');

        return function () {};
    });

For AMD dependencies, the extension ``.js`` is automatically added to modules,
so ``dependency1`` will be loaded from ``dependency1.js``.

.. note::
    A common alternate API is to define requirements when calling the ``define()``
    function. While sometimes shorter, this quickly becomes dreadful to read
    and is therefore considered an anti-pattern.

    For example (note the lack of readability)::

        define([ "require", "jquery", "blade/object", "blade/fn", "rdapi",
                 "oauth", "blade/jig", "blade/url", "dispatch", "accounts",
                 "storage", "services", "widgets/AccountPanel", "widgets/TabButton",
                 "widgets/AddAccount", "less", "osTheme", "jquery-ui-1.8.7.min",
                 "jquery.textOverflow"],
        function (require,   $,        object,         fn,         rdapi,
                  oauth,   jig,         url,         dispatch,   accounts,
                  storage,   services,   AccountPanel,           TabButton,
                  AddAccount,           less,   osTheme) {

        });

.. seealso::

    Asynchronous module definition
        https://en.wikipedia.org/wiki/Asynchronous_module_definition


Require.js
^^^^^^^^^^
RequireJS is perhaps the most used AMD loader. It is optimized for in-browser
use but can also be used with :ref:`Node` to build and optimize JS before
distributing.

.. seealso::

    RequireJS API
        http://requirejs.org/docs/api.html

    Using RequireJS with jQuery
        http://requirejs.org/docs/jquery.html

    RequireJS Optimizer
        http://requirejs.org/docs/optimization.html


.. _template-libraries:

Template libraries
------------------
Several client-side template languages exist, the most elementary one being
the one included in Underscore_.

Handlebars
^^^^^^^^^^
Handlebars is an extendable but compatible variant of the Moustache minimal
logic-less template library.

.. seealso::

    Handlebars
        http://handlebarsjs.com/

    Moustache
        http://mustache.github.io/


.. _mvc-libraries:

MVC/MVP libraries
-----------------

.. _backbone:

Backbone
^^^^^^^^
Backbone.js gives structure to web applications by providing **models** with
key-value binding and custom events, **collections** with a rich API of enumerable
functions, **views** with declarative event handling, and connects it all to your
existing API over a RESTful JSON interface.

Backbone requires Underscore_ and is commonly used with a
:ref:`templating library <template-libraries>` and a
:ref:`DOM library <dom-libraries>`.

.. seealso::

    Backbone.js
        http://backbonejs.org/


.. _underscore:

Underscore
----------
Underscore is a util library required by Backbone_, including a minimalist
template engine.

It provides 80-odd functions that support both the usual
functional suspects: map, select, invoke — as well as more specialized
helpers: function binding, javascript templating, deep equality testing,
and so on. It delegates to built-in functions, if present, so modern browsers
will use the native implementations of forEach, map, reduce, filter, every,
some and indexOf.

.. note::
    Several performance-optimized compatible drop-in replacements for
    Underscore_ exist which are *much* faster and are recommended over
    the original Underscore library: Lazy.js, Lo-Dash.

.. seealso::

    Underscore.js
        http://underscorejs.org/

    Lo-Dash
        http://lodash.com/

    Lazy.js
        http://danieltao.com/lazy.js/


.. index:: DOM

.. _dom-libraries:

DOM Libraries
-------------
The DOM (Document Object Model) is an in-memory representation of the HTML
structure in a web page, which can be accessed using so-called DOM libraries,
the best example of which is jQuery.

DOM libraries provide uniform access for iterating over, reading, manipulating
and responding to events on live elements in the browser.

.. seealso::

    jQuery
        http://jquery.com/

    DOM Introduction
        http://www.quirksmode.org/dom/intro.html

    DOM on Wikipedia
        https://en.wikipedia.org/wiki/Document_Object_Model


.. _zepto:

.. index::
    Zepto.js
    see: Zepto; Zepto.js

Zepto
^^^^^
Zepto is a minimalist JavaScript library for modern browsers with a largely
jQuery-compatible API. Because Zepto lacks support for Internet Explorer, it
is much smaller and faster than jQuery while providing largely
equivalent functionality.

As such, it can often be used as a drop-in replacement using the
following snippet for jQuery fallback on IE::

    <script>
    document.write('<script src=' +
    ('__proto__' in {} ? 'zepto' : 'jquery') +
    '.js><\/script>')
    </script>

.. seealso::

    Zepto.js
        http://zeptojs.com/


.. index::
    Node.js
    see: Node; Node.js

.. _node:

Node.js
-------
Node.js is a platform for easily building fast, scalable network applications
using JavaScript.

.. seealso::

    The Node Beginner Book
        http://www.nodebeginner.org/

    A guided introduction to Node.js
        https://www.youtube.com/watch?v=jo_B4LTHi3I

    Node.js API docs
        http://nodejs.org/api/


NPM
^^^
Node Package Manager. Installs, publishes and manages node programs.

By default, NPM installs packages and dependencies in the current directory,
yielding the equivalent of Python's VirtualEnv_. This is a particular
convenience when installing project dependencies, for example:

.. code-block:: console

    git clone git@github.com:alexyoung/nodepad.git nodepad
    cd nodepad
    npm install

    node app.js

This installs Nodepad_, a Node notepad part of a tutorial series on DailyJS_.

Alternately, to install packages globally use the ``-g`` option. For example::

    npm install -g yeomen

This makes sure the ``yo`` command of :ref:`yeoman`, :ref:`grunt` and other
commands are available regardless of the :ref:`cwd`.

.. _VirtualEnv: https://pypi.python.org/pypi/virtualenv
.. _DailyJS: http://dailyjs.com
.. _Nodepad: http://dailyjs.com/2010/11/01/node-tutorial/

Web application frameworks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
There exist several frameworks to aid in the development of Node web
applications. Some of these are:

* `express <http://expressjs.com/>`_
* `partial.js <http://www.partialjs.com/>`_
