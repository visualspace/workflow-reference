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
