==============================================================================
Deprecation: #46770 - Deprecate LocalImageProcessor::getTemporaryImageWithText
==============================================================================

Description
===========

The public method ``LocalImageProcessor::getTemporaryImageWithText()`` is marked for deprecation, it is directly
replaced by ``\TYPO3\CMS\Core\Imaging\GraphicalFunctions::getTemporaryImageWithText()``.


Impact
======

Calling ``LocalImageProcessor::getTemporaryImageWithText()`` will trigger a deprecation log message.

Affected installations
======================

TYPO3 Installations with custom extensions using the API of the File Abstraction Layer for custom image processing.

Migration
=========

Replace all calls to the method to the LocalImageProcessor with an instantiation of GraphicalFunctions and a call
to ``getTemporaryImageWithText()`` on the GraphicalFunctions object.
