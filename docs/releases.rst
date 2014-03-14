Prioritization and Release Plan
===============================
This discusses topics associated with new releases of Karaage and feature
requests.

Submission of Feature requests
------------------------------
Features requests that do not comply with these specifications will not be
considered unless the specifications are updated first.

Submitting patches that meet our submission guidelines will increase the
priority of the feature being incorporated.

..  actdiag::

   actdiag {
        A [label="Submit SRS change"]
        BB [label="Comunity consultation (optional)"]
        B [label="SRS change approved"]
        C [label="Submit compliance bug"]
        DD [label="Design change"]
        D [label="Submit patch"]
        EE [label="Comunity consultation (optional)"]
        E [label="Patch approved"]
        F [label="Close compliance bug"]
        A -> BB -> B -> C -> DD -> D -> EE -> E -> F

        lane {
           label = "Submitter"
           A
           C
           D
        }
        lane {
          label = "Karaage community"
          BB
          EE
        }
        lane {
           label = "Karaage team"
           B
           E
           F
        }
   }

The community consultation will only be used in cases where the proposed change
has wider consequences that could affect other Karaage users, at the discretion
of the Karaage maintenance team.

Prioritization of Feature requests
----------------------------------
Requests to change SRS or code that do not include patches, or where the
submitted patch is of poor quality and needs extra work:

*   From V3 staff will take priority over feature requests from non-paying
    external entities.
*   To increase the priority of a proposed feature,
    arrangements to sponsor the implementation can be made with V3 management.


Version numbers
---------------
Karaage version numbers are composed of three integers: major.minor.patch:

*   *major*: indicates a major release of Karaage. Such changes may have
    incompatible changes with previous releases. After a new major release, the
    previous version will continue to be supported and bugs fixed. Support for
    upgrading may not be supported for more then one major release at a time.
    For example, version 1 users may have to upgrade to version 2 before
    upgrading to version 3. Upgrading to a major

*   *minor*: a change in the minor version indicates significant, but not major,
    changes, e.g.  database migrations, may be involved in the upgrade. The old
    version will no longer be supported, however there shouldn't be any issues
    in upgrading.  Upgrading to a new minor release may require small amounts of
    downtime to do database migrations and/or update configuration.

*   *patch*: indicates bug fixes and/or other small changes. Some changes could
    involve fixing security issues. The old version will no longer supported, and
    should not be used any more. No changes should be required other then
    upgrading the package.

Release policy
--------------
New patch releases of Karaage are released most frequently. They are released
as required, depending on how important the changes are, and if it fixes
security issues.

New minor releases of Karaage are released according to demand, how important
the changes are, and if it fixes security issues. The aim is to release these
not more then one a month.

New major releases of Karaage will be made as required, but not before V3 has
upgraded its Karaage installation to at least the previous major release. The
aim is not to release more then one major release a year.
