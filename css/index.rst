.. highlight:: css

.. index:: ! CSS

.. _css:

Style sheets
============


.. _reset:

Browser reset
-------------
A CSS Reset (or “Reset CSS”) is a set of CSS rules that resets the styling of
all HTML elements to a consistent baseline across browsers.

.. seealso::
    * `What Is A CSS Reset? <http://www.cssreset.com/what-is-a-css-reset/>`_
    * `Eric Meyer's original Reset CSS <http://meyerweb.com/eric/tools/css/reset/>`_
    * :ref:`normalise.css`


.. _normalise.css:

normalise.css
^^^^^^^^^^^^^
A modern, HTML5-ready alternative to CSS resets.

Normalize.css makes browsers render all elements more consistently and in line
with modern standards. It precisely targets only the styles that need normalizing.

.. seealso:: http://necolas.github.io/normalize.css/


.. _sass:

Sass
----
Sass is an extension of CSS that adds power and elegance to the basic language.
It allows you to use variables_, `nested rules`_, mixins_, `inline imports`_, and more,
all with a fully CSS-compatible syntax. Sass helps keep large stylesheets
well-organized, and get small stylesheets up and running quickly,
particularly with the help of Compass_.

.. _variables: http://sass-lang.com/documentation/file.SASS_REFERENCE.html#variables_
.. _nested rules: http://sass-lang.com/documentation/file.SASS_REFERENCE.html#nested_rules
.. _mixins: http://sass-lang.com/documentation/file.SASS_REFERENCE.html#mixins
.. _inline imports: http://sass-lang.com/documentation/file.SASS_REFERENCE.html#import

.. seealso:: `Sass reference <http://sass-lang.com/documentation/file.SASS_REFERENCE.html>`_


.. _compass:

Compass
-------
Compass is a CSS authoring framework based on Sass_ providing:

* Cross browser CSS3 mixins that take advantage of available pre-spec vendor prefixes
* Mixins for common typography patterns.
* Mixins for other common styling patterns.
* An optional :ref:`reset` component.
* Page layout modules for: grid backgrounds, sticky footers, stretching.

.. seealso:: `Compass Reference <http://compass-style.org/reference/compass/>`_


.. _susy:

Susy
----
Susy is a responsive grid system for Compass_.

.. seealso::
    * `Using Susy with Yeoman <http://susy.oddbird.net/guides/getting-started/#start-yeoman>`_
    * `Susy documentation <http://susy.oddbird.net/>`_


CSS Workflow
------------
See: https://vimeo.com/15982903
