.. highlight:: scss

.. index:: ! CSS

.. _css:

Style sheets
============

Style Precedence
----------------
CSS Specificity is one of the most difficult concepts to grasp in Cascading Stylesheets. The different weight of selectors is usually the reason why your CSS-rules don’t apply to some elements, although you think they should have.

Every selector has its place in the specificity hierarchy. There are four distinct categories which define the specificity level of a given selector:

1. Inline styles (Presence of style in document).
   An inline style lives within your XHTML document. It is attached directly to the element to be styled. E.g. ``<h1 style="color: #fff;">``

2. IDs (# of ID selectors)
   ID is an identifier for your page elements, such as ``#div``.

3. Classes, attributes and pseudo-classes (# of class selectors).
   This group includes ``.classes``, ``[attributes]`` and pseudo-classes such as ``:hover``, ``:focus`` etc.

4. Elements and pseudo-elements (# of Element (type) selectors).
   Including for instance ``:before`` and ``:after``.

.. seealso::
    * `CSS Specificity: Things You Should Know <http://coding.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/>`_
    * `Understanding Style Precedence in CSS: Specificity, Inheritance, and the Cascade <http://www.vanseodesign.com/css/css-specificity-inheritance-cascaade/>`_

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

Media queries
^^^^^^^^^^^^^
As of 3.2 (the current release), Sass has smart support for `CSS3 media queries`_. This allows for patterns like::

    $information-phone: "only screen and (max-width : 320px)";

    @media #{$information-phone} {
      background: red;
    }

This compiles to::

    @media screen and (max-device-width: 320px) {
      background: red;
    }

.. _CSS3 media queries: http://webdesignerwall.com/tutorials/css3-media-queries

.. seealso:: http://thesassway.com/intermediate/responsive-web-design-in-sass-using-media-queries-in-sass-32


.. _compass:

Compass
-------
Compass is a CSS authoring framework based on Sass_ providing:

* Cross browser CSS3 mixins that take advantage of available pre-spec vendor prefixes
* Mixins for common typography patterns.
* Mixins for other common styling patterns.
* An optional :ref:`reset` component.
* Page layout modules for: grid backgrounds, sticky footers, stretching.

.. seealso::
    * `Compass Reference <http://compass-style.org/reference/compass/>`_


.. _grids:

Grid systems
------------
Several grid systems exist to make the life of web designers easier.
One of these is contained in :ref:`bootstrap`, another is provided by
Susy_.


.. _susy:

Susy
^^^^
Susy is a responsive grid system for Compass_.

.. seealso::
    * `Using Susy with Yeoman <http://susy.oddbird.net/guides/getting-started/#start-yeoman>`_
    * `Susy documentation <http://susy.oddbird.net/>`_


CSS Workflow
------------
See: https://vimeo.com/15982903
