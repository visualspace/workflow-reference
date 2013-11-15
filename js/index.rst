.. highlight:: js

.. index::
    ! JavaScript
    see: JS; JavaScript

.. _js:

JavaScript
==========

.. _template-libraries:

Template libraries
------------------
Several client-side template languages exist, the most elementary one being
the one included in Underscore_.

Handlebars
^^^^^^^^^^
Handlebars is an extendable but compatible variant of the Moustache_ minimal
logic-less template library.

.. seealso::
    * `Handlebars <http://handlebarsjs.com/>`_
    * `Moustache <http://mustache.github.io/>`_

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
    * `Backbone.js <http://backbonejs.org/>`_

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
    the original Underscore library: `Lazy.js`_, `Lo-Dash`_.

.. seealso::
    * `Underscore.js <http://underscorejs.org/>`_
    * `Lo-Dash <http://lodash.com/>`_
    * `Lazy.js <http://danieltao.com/lazy.js/>`_

.. index:: DOM

.. _dom-libraries:

DOM Libraries
-------------
The DOM (Document Object Model) is an in-memory representation of the HTML
structure in a web page, which can be accessed using so-called DOM libraries,
the best example of which is jQuery_.

DOM libraries provide uniform access for iterating over, reading, manipulating
and responding to events on live elements in the browser.

.. seealso::
    * `jQuery <http://jquery.com/>`_
    * `DOM Introduction <http://www.quirksmode.org/dom/intro.html>`_
    * `DOM on Wikipedia <https://en.wikipedia.org/wiki/Document_Object_Model>`_

.. _zepto:

.. index::
    Zepto.js
    see: Zepto; Zepto.js

Zepto
^^^^^
Zepto is a minimalist JavaScript library for modern browsers with a largely
jQuery_-compatible API. Because Zepto lacks support for Internet Explorer, it
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
    * `Zepto.js <http://zeptojs.com/>`_
