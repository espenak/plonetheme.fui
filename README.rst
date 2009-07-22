===============================================================================
README
===============================================================================

Plone theme written for *Fagutvalget ved Institutt for informatikk*
(http://fui.ifi.uio.no). The theme is available at these addresses:

    - http://pypi.python.org/pypi/plonetheme.fui/
    - http://github.com/espenak/plonetheme.fui/

The only file I have modified from the default plone3 theme, except some minor
adjustments to ``setup.py``, is
``plonetheme/fui/browser/stylesheets/main.css``. I have simply inspected the
xhtml source produced by plone, and made the CSS by the trial and error method.


Install
-------

You can install this theme in Plone using buildout.

    1. Add ``plonetheme.fui`` to ``buildout.cfg``::

        [buildout]
        ...
        eggs =
            ...
            plonetheme.fui

        [instance]
        ...
        zcml = 
            ...
            plonetheme.fui

    2. Run (maybe backup first..)::

        ~$ buildout -n

    3. Install the plugin using *Site Setup* in your Plone site.



Release a new version (for developers)
--------------------------------------

Release a new version to pypi.python.org with::

    ~$ python setup.py egg_info -RDb "" sdist upload
