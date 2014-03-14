Introduction
============
This document is intended to specify a set of requirements for Karaage[SRS_].


Purpose
-------
This documentation is intended to set the scope of Karaage, to allow other
people to see where it is heading, while reducing the potential for feature
creep.


Errors
------
If there are any errors in this document, these needs to be addressed. Errors
generally will fall into one of three categories:

*   Features that are required and not specified. This should be addressed
    by submitting changes to this document.
*   Mismatch between what is described here and how Karaage operates. If
    Karaage is incorrect, this should be addressed with a bug report. If this
    specification is incorrect, then this should be rectified by submitting
    changes to this document.
*   Errors in the documentation. These should be rectified by submitting
    changes to this document.


Scope
-----
Karaage is a web based interface to create a system for management of users for
a supercomputer or cloud system. As a result it needs to interface to various
databases, such as LDAP, to write account information.

Karaage needs to be able to delegate certain functions to authorised people
(such as approving accounts), as appropriate for local installation
requirements.

There is also the requirement to be able to monitor super computer usage
information. At present this means keeping track of information concerning
cluster jobs running on a super computer. This function needs to be kept
optional, as it may not be relevant for all sites.


Definitions
-----------
See :doc:`glossary`.

Please note when reading this, that the terms :term:`person`, :term:`people`,
and :term:`account` have strict definitions for use by Karaage.

Overview
--------
In the next chapter, :doc:`overall`, we first define the overall system.

Then, in chapter :doc:`requirements`, we give the external interface
requirements, followed by a brief description of the Karaage components and
features.

After that, in chapter :doc:`releases` discusses the release plan.

Finally, in chapter :doc:`future` discusses future changes to this document.

References
----------

.. [SRS] http://en.wikipedia.org/wiki/Software_requirements_specification
