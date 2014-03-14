Overall description
===================
This is the broad overall description of Karaage and its requirements.


Product perspective
-------------------
Karaage consists of web interface. There are three basic views:

*   If an unauthenticated user sees the site, they can login or apply for an
    account.

*   If an :term:`administrators` logs in, the see a menu appropriate to
    administration.

*   If another :term:`person` logs in, the see a menu appropriate to
    non-administration duties.

Furthermore, it is possible to have two separate interfaces:

*   *karaage-admin*: user must be an administrator to access this site.

*   *karaage-registration*: user is treated as non-administrator even if
    they have administration rights.

Karaage stores information about people, accounts, institutes, projects,
software and usage and stores it in a database. This information is them
replicated to external databases as per :term:`local requirements`. These
could include LDAP, Slurm, Gold, and OpenStack Keystone databases.

Product functions
-----------------
:term:`People` use Karaage to apply for project access, login, change their
password, reset their password, view usage information

Some people may have roles that allow for additional access. :term:`Project
leaders` can approve requests to join their project. :term:`Institute
delegates` can approve requests to create new projects for their institute.

:term:`Administrators` use Karaage to add, edit, and view information
concerning people, accounts, institutes, projects, software and usage.


.. _user_characteristics:

User Characteristics
--------------------
Karaage is aimed at different sets of target users:

*   *administrators*: Should have a basic understanding of the installation,
    data stores used, and what uses these data stores. Should understand the
    terms used in the :doc:`glossary`.

*   *end users*: Should have a basic understanding of what a Unix account is. In
    practise the experience and knowledge of these user's may vary
    considerably.


Contraints, assumptions and dependancies
----------------------------------------
This section documents any constraints Karaage has, any assumptions that can be
made, and external dependencies required.

.. _operating_system_dependancies:

Operating system dependancies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The servers used for Karaage should be able to run on Debian Wheezy, using
using the Python 2.7 language.

A MySQL database is required for storing Karaage data.

.. todo:

    RHEL6 support.

Assumptions
~~~~~~~~~~~
Karaage is a software project only. Project management is expected for
obtaining appropriate hardware, installation and customisation to :term:`local
requirements` at individual sites.
