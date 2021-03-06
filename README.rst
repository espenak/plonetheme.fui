===============================================================================
README
===============================================================================

Plone theme written for *Fagutvalget ved Institutt for informatikk*
(http://fui.ifi.uio.no). The theme is available at these addresses:

    - http://pypi.python.org/pypi/plonetheme.fui/
    - http://github.com/espenak/plonetheme.fui/

The only file I have modified from the default plone3 theme, except some minor
adjustments to ``setup.py`` and ``main_template.pt``, is
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

    4. Add the following lines at the end of the Styles box in
       ``Site setup --> Visual editor --> Config``::
       
           Image float left|img|float-left
           Image float right|img|float-right
           Bordered image float left|img|bordered-float-left
           Bordered image float right|img|bordered-float-right

    (5.) Add the following styles to the FCKeditor styles::

        <Style name="Image float left" element="img">
          <Attribute name="class" value="float-left" />
        </Style>
        <Style name="Image float right" element="img">
          <Attribute name="class" value="float-right" />
        </Style>
        <Style name="Bordered image float left" element="img">
          <Attribute name="class" value="bordered-float-left" />
        </Style>
        <Style name="Bordered image float right" element="img">
          <Attribute name="class" value="bordered-float-right" />
        </Style>


Code syntax highlighting
------------------------

The theme loads prettify.js (http://code.google.com/p/google-code-prettify/).
Add the *prettify* class to your <pre> blocks to get syntax hightlighting.



For developers
--------------

Release a new version to pypi.python.org with::

    ~$ python setup.py egg_info -RDb "" sdist upload


You can run plone in the foreground with:

    ~$ plonectl fg

Note that resources are not added unless you reinstall the product.


Tutorials on theme development might be found on http://plone.org, but I found these extra useful:

- http://plone.org/documentation/kb/how-to-create-a-plone-3-theme-product-on-the-filesystem
- http://plone.org/documentation/kb/how-to-install-a-3-x-theme-using-buildout
