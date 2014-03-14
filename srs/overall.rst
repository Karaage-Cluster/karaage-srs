Overall description
===================
This is the broad overall description of Karaage and its requirements.


Product perspective
-------------------
Karaage consists of web interface. There are three basic views:

*   If an unauthenticated user sees the site, they can login or apply for an
    account.

*   If an :term:`administrators` logs in, the see a menu appriopriate to
    administration.

*   If another :term:`person` logs in, the see a menu appriopriate to
    non-administration duties.

Futhermore, it is possible to have two seperate interfaces:

*   *karaage-admin*: user must be an administrator to access this site.

*   *karaage-registration*: user is treated as non-administrator even if
    they have administration rights.

Karaage stores information about people, accounts, institutes, projects,
software and usage and stores it in a database. This information is them
replicated to external databases as per :term:`local requirements`. These
could include LDAP, Slurm, Gold, and Openstack Keystone databases.


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
    datastores used, and what uses these data stores. Should understand the
    terms used in the :doc:`glossary`.

*   *end users*: Should have a basic understanding of what a Unix account is. In
    practise the experience and knowledge of these user's may vary
    considerably.


Contraints, assumptions and dependancies
----------------------------------------
It must be possible to install Karaage at different sites. It should be
possible to customize every site to match their own :term:`local requirements`,
as long as it falls under the defined scope of Karaage, as per this
specifiction. It should be possible to to do this customization using well
defined mechanisms that do not break with minor releases of Karaage, or have a
well defined upgrade path for major releases of Karaage.

