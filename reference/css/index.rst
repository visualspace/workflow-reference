.. highlight:: scss

.. index:: ! CSS

.. _css:

Style sheets
============

.. seealso:: `Pears are common patterns of markup & style <http://pea.rs/>`_

Modular architecture
--------------------
Every project needs some organization. Throwing every new style you
create onto the end of a single file would make finding things more
difficult and would be very confusing for anybody else working on the
project.

.. seealso::

    Scalable and Modular Architecture for CSS (SMACSS)
        http://smacss.com/book/
    The Sass Way
        http://thesassway.com/

File structure
^^^^^^^^^^^^^^
There are several ways of organizing CSS into files. Whereas
traditionally it was easier to put all the styles for a single site
either into a single file or to simply concatenate and compress a
bunch of files, modern style languages like Sass_ and Less allow
for much smarter and potentially faster ways to set things up.

One way to setup a (S)CSS file structure is a combination of an
'onion' and a modular pattern. The modular pattern assures maximal
reusability of design patterns and common solutions to common problems
(:ref:`DRY <dry>`). The onion model helps us steer clear of
:ref:`precedence <style-precedence>` issues.

While being a work in progress, the import order in a hypothetical
``main.scss`` would look as follows::

    // Modular mixins. These should generate no CSS of themselves but merely
    // make mixins, variables and functions available and can be reused
    // from site to site.
    @import "buttons";
    @import "shades";
    ...

    // Project-specific modules (again: not producing any actual CSS output)
    @import "variables";
    @import "colours";
    @import "fonts";

    // Common site-wide components
    @import "reset"; // Browser reset
    @import "tags"; // Tag selectors
    @import "grid"; // Grid system
    @import "classes"; // Common classes (object-based / SMACSS)
    @import "ids"; // Common ID-referenced styles (keep these to a minimum)

    // App-specific overrides of common ids and classes
    // (Try to minimize tag selectors here)
    @import "admin";
    @import "shop";
    @import "blog";
    ...

    // Media-specific overrides of tags, classes, apps and grid.
    @import "media";

.. warning::
    This is a very early sketch of a mere candidate of a CSS structure which
    is untested and not yet ready for actual implementation. Unless you're
    brave.

.. seealso::

    How to structure a Sass project
        http://thesassway.com/beginner/how-to-structure-a-sass-project

Naming conventions
^^^^^^^^^^^^^^^^^^
.. seealso::

    Modular CSS naming conventions
        http://thesassway.com/advanced/modular-css-naming-conventions

.. _style-precedence:

Style Precedence
----------------
CSS Specificity is one of the most difficult concepts to grasp in Cascading
Stylesheets. The different weight of selectors is usually the reason why your
CSS-rules don’t apply to some elements, although you think they should have.

Every selector has its place in the specificity hierarchy. There are four
distinct categories which define the specificity level of a given selector:

1. Inline styles (Presence of style in document).
   An inline style lives within your XHTML document. It is attached directly
   to the element to be styled. E.g. ``<h1 style="color: #fff;">``

2. IDs (# of ID selectors)
   ID is an identifier for your page elements, such as ``#div``.

3. Classes, attributes and pseudo-classes (# of class selectors).
   This group includes ``.classes``, ``[attributes]`` and pseudo-classes such
   as ``:hover``, ``:focus`` etc.

4. Elements and pseudo-elements (# of Element (type) selectors).
   Including for instance ``:before`` and ``:after``.

.. seealso::

    CSS Specificity: Things You Should Know
        http://coding.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/

    Understanding Style Precedence in CSS: Specificity, Inheritance, and the Cascade
        http://www.vanseodesign.com/css/css-specificity-inheritance-cascaade/

.. _reset:

Browser reset
-------------
A CSS Reset (or “Reset CSS”) is a set of CSS rules that resets the
styling of all HTML elements to a consistent baseline across browsers.

.. todo::
    Include one of the following alternatives as bad practise and the
    others as explicitly deprecated.

    * :ref:`normalise.css`?
    * :ref:`Compass`' CSS reset
    * Eric Meyer's original

.. seealso::

    What Is A CSS Reset?
        http://www.cssreset.com/what-is-a-css-reset/

    Eric Meyer's original Reset CSS
        http://meyerweb.com/eric/tools/css/reset/

    :ref:`normalise.css`


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

    Compass Reference
        http://compass-style.org/reference/compass/


.. _grids:

Grid systems
------------
Several grid systems exist to make the life of web designers easier. We currently recommend the usage of the :ref:`susy` responsive grid system, unless :ref:`bootstrap` is used, which works better with the already included grid system.

.. _susy:

Susy
^^^^
Susy is a responsive grid system for Compass_.

.. seealso::

    Using Susy with Yeoman
        http://susy.oddbird.net/guides/getting-started/#start-yeoman

    Susy documentation
        http://susy.oddbird.net/


CSS Workflow
------------

See: https://vimeo.com/15982903


.. _viewport:

Viewport
--------
For modern web development, we have to account for several types of viewports:

1. The visual viewport; the part of the page that's currently on-screen.
2. The layout viewport; the viewport referenced to in CSS.
3. The ideal viewport, where the layout viewport is equal to the visual viewport.

In responsive designs we generally want an ideal viewport and adjust the elements to the available pixels instead of zooming the whole site. For this we use the viewport meta tag in the HTML header to disable zoom and set the width of the layout viewport equal to that of the device::

    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">

For full-screen applications which are not meant to scroll, also set the height of the viewport to the device height::

    <meta name="viewport" content="width=device-width, height=device-height, initial-scale=1, maximum-scale=1, user-scalable=no">

.. note::
    The device pixels (``device-width`` and ``device-height``) are not necessarily equal to actual screen pixels due to the device pixel ratio. See :ref:`device-independent-pixels`.

.. seealso::

    CSS Device Adaptation With @viewport
        http://blog.teamtreehouse.com/thinking-ahead-css-device-adaptation-with-viewport

    Stop using the viewport meta tag (until you know how to use it)
        http://blog.javierusobiaga.com/stop-using-the-viewport-tag-until-you-know-ho

    Mozilla: Using the viewport meta tag to control layout on mobile browsers
        https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag

    Mobiles and Tablets – Viewport Sizes
        http://i-skool.co.uk/mobile-development/web-design-for-mobiles-and-tablets-viewport-sizes/

    Browser compatibility — viewports
        http://www.quirksmode.org/mobile/tableViewport.html

    :ref:`device-independent-pixels`


.. _device-independent-pixels:

Device Independent Pixels
-------------------------

.. todo::
    There are several references here, with varied quality and usability. Please remove what's not usable and summarise the
    useful bits.

.. seealso::

    A Pixel is not a Pixel by Peter-Paul Koch
        http://fronteers.nl/congres/2012/sessions/a-pixel-is-not-a-pixel-peter-paul-koch

    Towards A Retina Web
        http://coding.smashingmagazine.com/2012/08/20/towards-retina-web/

    A Pixel Identity Crisis
        http://alistapart.com/article/a-pixel-identity-crisis/

    :ref:`device-pixel-ratio`

    :ref:`viewport`


.. _device-pixel-ratio:

Device pixel ratio
------------------

``devicePixelRatio`` is the ratio between physical pixels and device-independent pixels (dips) on the device:

.. code-block:: js

    window.devicePixelRatio = physical pixels / dips

.. seealso::

    devicePixelRatio
        http://www.quirksmode.org/blog/archives/2012/06/devicepixelrati.html

    More about devicePixelRatio
        http://www.quirksmode.org/blog/archives/2012/07/more_about_devi.html

    :ref:`device-independent-pixels`

    :ref:`viewport`



