Changelog
=========

2.3 (unreleased)
----------------

- Nothing changed yet.


2.2 (2016-12-19)
----------------

- Move translations to ``locales/`` to be able to add/modify
  translations in none-Zope2 packages too [fRiSi]


2.1 (2014-10-23)
----------------

- Support different image fieldnames within the same component (fixed js scope
  bug) and use .component as selector for an item (cropping is compatible with
  raptus.article.listing and gallery this way)

2.0 (2014-07-28)
----------------

- Introduce a new marker interface (INamedDefaultComponent) and ready
  to use adapter implementation to allow simple registrations of default
  components by using named adapters (this fixes #5) [skaeser]

- Make textfield a primary field (as it's the case for default document type)
  to prevent certain versions of plone's TinyMCE integration to raise
  AttributeErrors when searching for anchors (this fixes #3) [fRISi]


2.0b19 (2014-07-22)
-------------------

- Refactored the related items component of raptus articles (fixed issue #7).

  The previous implementation was based on the deprecated python
  script named ``computeRelatedItems``, no more available
  on Plone 4.3.2. [davidemoro]


2.0b18 (2014-06-16)
-------------------

- Show Link to plone.app.imagecropping croppingeditor if the component
  adds a ``crop`` property to the manageable list items pointing to the
  editor (eg path/to/image/@@croppingeditor?scalename=thumb)

  The croppingeditor is opened in an overlay and the cropped image
  gets updated when the editor is closed. [fRiSi]

- rename resource ``component.js`` to ``raptus.article.component.js`` to prevent
  name conflicts. [fRiSi]

2.0b17 (2013-12-17)
-------------------

* The article view now implements IViewView to support plone.app.discussion when
  manually activated see:
  http://stackoverflow.com/questions/10402918/can-not-activate-discussions-on-plone-dexterity-types-folderish
* Replaced deprecated getIcon() with getIconExprObject()


2.0b16 (2013-07-22)
-------------------

* CSS adjustments (added z-index for article-toggle and article-manage)
* Plone 4.3 compatibility [tmassman]


2.0b15 (2013-07-02)
-------------------

* Made some minor CSS adjustments
* Implemented drag'n'drop for raptus.article.table


2.0b14 (2013-07-02)
-------------------

* Removed event dispatch function to prevent double event notifications


2.0b13 (2013-07-01)
-------------------

* Component management reimplementation
* Added drag'n'drop support
* Added component activated and deactivated events
* PEP 8


2.0b12 (2013-05-03)
-------------------

* Improved component filter to no longer update every viewlet when filtering
  and sorting

2.0b11 (2013-03-11)
-------------------

* Italian translations [vito80ba]

2.0b10 (2012-03-21)
-------------------

* Changed permission for view of articles from zope.Public to zope2.View
  to prevent odd behaviour if accessing private article with title and
  description hidden where a completely unstyled login form was presented

2.0b9 (2012-01-23)
------------------

* plone 4.1 compatibility by importing cmfcore permissions

2.0b8 (2011-03-21)
------------------

* Added links to the manageable adapter to show and hide items in a component

2.0b7 (2011-01-20)
------------------

* Fixed AttributeError raised if a Viewlet has been customized ttw, which resulted
  in a TTWViewletRenderer object which has no __name__ attribute
  (Thanks to Ron Zayac for reporting it)

2.0b6 (2010-11-25)
------------------

* Fix Namespace on related items

2.0b5 (2010-11-10)
------------------

* Added French translations

2.0b4 (2010-10-21)
------------------

* Updated readme and manual

2.0b3 (2010-10-20)
------------------

* First public release
