Design patterns
===============
A design pattern is a general reusable solution to a commonly occurring problem within a given context.

.. seealso::
    * `Design patterns on Wikipedia <https://en.wikipedia.org/wiki/Software_design_pattern>`_
    * `Django Design Philosophies <https://docs.djangoproject.com/en/dev/misc/design-philosophies/>`_
    * `Seven Principles Of Software Development <http://c2.com/cgi/wiki?SevenPrinciplesOfSoftwareDevelopment>`_

.. _dry:

Don't Repeat Yourself
---------------------
Every distinct concept and/or piece of data should live in one, and only one, place. Redundancy is bad. Normalization is good.

The framework, within reason, should deduce as much as possible from as little as possible.

.. seealso::
    * `DRY on the Portland Pattern Repository <http://c2.com/cgi/wiki?DontRepeatYourself>`_
    * `DRY on Wikipedia <https://en.wikipedia.org/wiki/Don't_repeat_yourself>`_

.. _kiss:

Keep It Simple, Stupid!
-------------------------
Design is not a haphazard process. There are many factors to consider in any design effort. All design should be as simple as possible, but no simpler. This facilitates having a more easily understood, and easily maintained system. This is not to say that features, even internal features, should be discarded in the name of simplicity. Indeed, the more elegant designs are usually the more simple ones. Simple also does not mean "quick and dirty." In fact, it often takes a lot of thought and work over multiple iterations to simplify. The payoff is software that is more maintainable and less error-prone.

.. seealso::
    * `KISS on Wikipedia <https://en.wikipedia.org/wiki/KISS_principle>`_
