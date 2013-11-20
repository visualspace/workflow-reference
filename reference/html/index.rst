.. highlight:: html

.. index:: ! HTML

.. _html:

HTML
====

HTML5
-----

.. seealso::

    HTML5 Rocks
        http://www.html5rocks.com/

    HTML5 Doctor
        http://html5doctor.com/

    W3Schools
        http://www.w3schools.com/


.. _favicon:

Favicon
^^^^^^^

.. todo:: Document favicon best practises.


.. index:: DOCTYPE

Doctype
^^^^^^^
When creating pages, make sure to use a Doctype declaration. For HTML5 this
means *all* HTML files should start with::

    <!DOCTYPE html>

.. warning::
    Before the doctype declaration, no spaces, characters or other content is allowed.

.. seealso::

    Doctype at HTML5 Doctor
        http://html5doctor.com/element-index/#doctype


App Cache
^^^^^^^^^
This explicitly allows browsers to download web application for offline
availability. This uses a so-called cache manifest which looks like this::

    # <VERSION IDENIFIER>
    CACHE MANIFEST
    FALLBACK:
    # This will cause any uncached URL to be substituted with offline.html
    / /offline.html
    NETWORK:
    # These resources will only be available online.
    /checking.cgi
    CACHE:
    # These resources will be downloaded in the background and cached
    /offline.html
    /test.css
    /test.js
    /test.png

.. note::
    The cached files are only updated when the contents of the
    manifest file have changed. Hence, it is essential that a some kind of
    version identifier or last modified date be added in a comment in the
    file.

.. note::
    Using a cache manifest causes the cached files to be loaded instead of the
    online version of files, while uploads are downloaded in the background.
    Updated files will only be available after a reload of the page, which
    can be automated using JavaScript.

.. note::
    For HTML5 offline app cache to function it is absolutely essential that
    the MIME type be set to `text/cache-manifest`.

.. seealso::

    Cache manifest in HTML5
        https://en.wikipedia.org/wiki/Cache_manifest_in_HTML5

    A Beginner's Guide to Using the Application Cache
        http://www.html5rocks.com/en/tutorials/appcache/beginner/

Video
^^^^^

.. seealso::

    HTML5 Video at W3Schools
        http://www.w3schools.com/html/html5_video.asp

    Video.js
        http://www.videojs.com/

Responsive images
^^^^^^^^^^^^^^^^^
Within HTML5, several tools are available to support multi-resolution images, each one complementing the other. For example::

    <picture>
        <source srcset="med.jpg 1x, med-hd.jpg 2x" media="(min-width: 40em)" />
        <source srcset="sm.jpg 1x, sm-hd.jpg 2x" />
        <img src="fallback.jpg" alt="" />
    </picture>

This snippet uses the ``<picture>`` element together with the ``srcset`` attribute.

.. todo::
    This section suggests several alternate approaches for responsive images. Add a recommendation for a particular approach or a proper argumentation allowing sensible decisions.

.. seealso::

    W3C: Use Cases and Requirements for Standardizing Responsive Images
        http://usecases.responsiveimages.org/


.. _srcset:

Srcset
~~~~~~
The srcset attribute allowed developers to specify a list of sources for an image attribute, to be delivered based on the pixel density of the user’s display::

    <img src="low-res.jpg" srcset="high-res.jpg 2x">

.. seealso::

    WebKit Has Implemented srcset, And It’s A Good Thing
        http://mobile.smashingmagazine.com/2013/08/21/webkit-implements-srcset-and-why-its-a-good-thing/

    :ref:`srcset-polyfill`

    :ref:`device-pixel-ratio`


.. _picture:

Picture
~~~~~~~
The picture element is an image container whose source content is determined by one or more CSS media queries::

    <picture>
        <source src="med.jpg" media="(min-width: 40em)" />
        <source src="sm.jpg" />
        <img src="fallback.jpg" alt="" />
    </picture>

.. seealso::

    HTML5 adaptive images: end of round one
        http://html5doctor.com/html5-adaptive-images-end-of-round-one/

    HTML5 <PICTURE> ELEMENT
        http://html5hub.com/html5-picture-element/

    :ref:`picturefill`

    W3C
        http://www.w3.org/TR/2013/WD-html-picture-element-20130226/
