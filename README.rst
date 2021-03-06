==============================================================
Menuplaceholder: placeholder menu items for Mezzanine
==============================================================

About
-----

The **menuplaceholder** application allows users to add placeholders to the menu
of a `Mezzanine <http://mezzanine.jupo.org/>`_ CMS website. Menu placeholders
are "dummy" menu items, which can be used for organising submenus. Users can
view them (and their children); unlike other types of menu items (such as those
for rich text pages), users cannot click on placeholders to open them.
Menu placeholders are provided to structure the hierarchy of
pages on a site, but are not used to provide content.

The **menuplaceholder** app works with the following things:

* Primary menus
* Mobile menus
* Dropdown menus
* Footers
* Breadcrumbs


Installation and usage
-----------------------------

You can either go::

  pip install menuplaceholder

Or download this source and go::

  python setup.py install

Then add ``"menuplaceholder"`` to ``INSTALLED_APPS`` in the settings.py file
for your Django installation, preferably *at the beginning*. Afterwards::

  python manage.py makemigrations menuplaceholder
  python manage.py migrate

Once this is done, adding a placeholder menu item (or ten) is trivial.

* Go to the Mezzanine dashboard.
* Under *Content*, click on *Pages* in order to "Select Page to change".
* Pick the part of the menu hierarchy you wish to add a menu placeholder, and
  click on "Add...". The dropdown menu now have a new item: "Menu placeholder".
  Select it.
* Choose a *Title* and then click on *Save*.

Note: If you place ``"menuplaceholder"`` in ``INSTALLED_APPS`` after
``"mezzanine.pages"``, you will find your dummy menu items clickable (and
thus not dummy menu items at all). That's because the main magic of this app is
rewriting the default Mezzanine menu templates, and if you put
``"mezzanine.pages"`` first, it "wins". However, if you put ``"menuplaceholder"``
first, it should take priority.

Dependencies
-------------
The **menuplaceholder** app has been trialled with both Python 2.7 and 3.5.
The other dependencies are:

* Django (1 . *x*; has not been tested on 2. *x*)
* Mezzanine (4 . *x*)

Versions
--------

* 0.1 (April 5th 2018) - Initial release. (Bug fix version 0.1.6 on April 8th.)

Copyright
---------

Copyright (c) 2017-2018
`Peter Murphy <http://www.pkmurphy.com.au/>`_
<peterkmurphy@gmail.com>.
