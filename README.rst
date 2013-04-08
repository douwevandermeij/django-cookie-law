==================
django-cookie-law
==================

django-cookie-law helps your Django project comply with the
`EU cookie regulations <http://www.aboutcookies.org/default.aspx?page=3>`_.

At the moment this application just displays cookie information banner until it is
dismissed by the user. There are future plans to allow user to choose whether
he wants to continue browsing the site using cookies or browse the site in
cookieless mode.

.. warning:: Above means the app can be incompatible with your local cookie
             law regulations. Consult your lawyer.

Contributions and comments are welcome using Github at:
http://github.com/centralniak/django-cookie-law

Please note that django-cookie-law requires:

- Django >= 1.2

Installation
============

#. ``pip install django-cookie-law``
#. Add ``'cookielaw'`` to ``INSTALLED_APPS``
#. Run ``collectstatic`` (Django 1.3+) or copy the statics to your media directory
#. Add ``cookielaw/js/cookielaw.js`` to the markup directly or via your asset
   manager such as ``django-pipeline`` or ``django-compressor``

Configuration
=============

If you want to use our default template, add ``cookielaw/css/cookielaw.css`` to
the markup and you should see the cookie law banner at the top of the page until
you dismiss it with the cross icon in the top-right. Chances are, you'll like
to change the text and/or CSS.

.. note:: The default template will change to a
`Twitter Bootstrap <http://twitter.github.io/bootstrap/>`_ compatible one.

To change the markup, just add a template named ``cookielaw/banner.html`` and
make sure it is loaded before the default template (for example put the
``django.template.loaders.filesystem.Loader`` before
``django.template.loaders.app_directories.Loader`` and add your new template
to any of the ``TEMPLATE_DIRS``).

To change the CSS, just write your own rules and don't like the default
stylesheet anywhere.

Bugs & Contribution
===================

Please use Github to report bugs, feature requests and submit your code:
http://github.com/TyMaszWeb/django-cookie-law

:author: Piotr Kilczuk
:date: 2013/04/08