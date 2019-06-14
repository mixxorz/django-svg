django-inline-svg |latest-version|
==================================

|build-status| |software-license|

A simple plugin that adds an ``svg`` template tag to inline your SVGs in your
Django templates.

Update 2019: Don't fear the lack of updates. This library still works. I use it for every project.


Installation
------------

Install it from pypi.

::

    $ pip install django-inline-svg

Add ``svg`` to your ``INSTALLED_APPS``.

::

    INSTALLED_APPS = (
        ...
        'svg',
        ...
    )

Usage
-----

Store your SVGs in folder named ``svg`` at the root of any of your static file
directories.

::

    my_app
    |-- static
    |   |-- svg
    |       |-- logo.svg
    |       |-- check.svg
    |       |-- cross.svg

Use the ``svg`` template tag.

::

    {% load svg %}

    <h1 class="logo">{% svg 'logo' %}</h1>

You can set ``SVG_DIRS`` to control where to look for your svgs.

::

    # settings.py

    SVG_DIRS = [
        os.path.join(BASE_DIR, 'my-svgs')
    ]

Support
-------

The tests are run against Django 1.8 to 2.0 on Python 2.7, 3.4, 3.5, 3.6.

License
-------

MIT

.. |latest-version| image:: https://img.shields.io/pypi/v/django-inline-svg.svg
   :target: https://pypi.python.org/pypi/django-inline-svg/
   :alt: Latest version
.. |build-status| image:: https://img.shields.io/travis/mixxorz/django-inline-svg/master.svg
   :target: https://travis-ci.org/mixxorz/django-inline-svg
   :alt: Build status
.. |software-license| image:: https://img.shields.io/pypi/l/django-inline-svg.svg
   :target: https://github.com/mixxorz/django-inline-svg/blob/master/LICENSE
   :alt: Software license
