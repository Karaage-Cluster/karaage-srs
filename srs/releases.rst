Prioritization and Release Plan
===============================
This discusses topics associated with new releases of Karaage and feature
requests.

Prioritization of Feature requests
----------------------------------
Feature requests from V3 staff will take priority over feature requests from
non-paying external entities. To increaase the priority of a feature,
arrangements can be made with V3 management. Submitting patches that meet our
submission guidelines will also increase the priority of the feature being
incorporated.

Version numbers
---------------
Karaage version numbers are composed of three integers: major.minor.patch:

*   *major*: indicates the a major release of Karaage. Such changes may have
    incompatable changes with previous releases. After a new major release, the
    previous version will continue to be supported and bugs fixed. Support for
    upgrading may not be supported for more then one major release at a time.
    e.g. version 1 users may have to upgrade to version 2 before upgrading to
    version 3. Upgrading to a major

*   *minor*: a change in the minor version indicates significant, but not major,
    changes, e.g.  database migrations, may be involved in the upgrade. The old
    version will no longer be supported, however there shouldn't be any issues
    in upgrading.  Upgrading to a new minor release may require small amounts of
    downtime to do database migrations and/or update configuration.

*   *patch*: indicates bug fixes and/or other small changes. Some changes could
    involve fixing security issues. The old version will no longer supported, and
    should not be used anymore. No changes should be required other then
    upgrading the package.

Release policy
--------------
