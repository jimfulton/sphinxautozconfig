*************************
Spinx support for ZConfig
*************************

For more information on ZConfig, see: https://pypi.python.org/pypi/ZConfig

Initially (and probably permanently :) ) This consists of a
``zconfigsectionkeys`` directive for rendering documentation for
ZConfig section keys.

Usage
*****

Install the ``j1m.sphinxautozconfig`` package.

Include ``'j1m.sphinxautozconfig'`` in the list of extensions in your
sphinx configuration::

  extensions = ['j1m.sphinxautozconfig']

Where you want the documentation for the keys of a ZConfig section,
use the zconfigsectionkeys directive::

  .. zconfigsectionkeys:: PACKAGE_NAME XML_FILE_NAME SECTION_NAME

where:

PACKAGE_NAME
  The name of the Python package containing the XML file.

XML_FILE_NAME
  The name of an XML file containing section definitions.  Typically,
  this is ``cpmponent.xml``.

SECTION_NAME
  The name of the section to render documentation for.

For example, to render key documentation for the ZODB filestorage section::

  .. zconfigsectionkeys:: ZODB component.xml filestorage

Changes
*******

0.1.0 (2016-09-07)
==================

Initial release
