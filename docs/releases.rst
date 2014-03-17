Prioritization and Release Plan
===============================
This discusses topics associated with new releases of Karaage and feature
requests.


Feature requests
----------------
This section discusses the requirements for getting new features in Karaage.
There are two basic steps:

#.  The requirements of the feature should be included in a release of the SRS.
#.  The feature needs to be included in a release of Karaage.

Prioritization of Feature requests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Requests to change SRS or code that do not include patches, or where the
submitted patch is of poor quality and needs extra work:

*   From V3 staff will take priority over feature requests from non-paying
    external entities.
*   To increase the priority of a proposed feature,
    arrangements to sponsor the implementation can be made with V3 management.


SRS change requirements
-----------------------
This section documents to requirements for generating new versions of the SRS.


..  actdiag::
    :maxwidth: 520

    actdiag {
        A [label="1. Submit request"]
        B [label="2. Modify SRS"]
        BB [label="2. Modify SRS"]
        BA [label="2. Modify SRS"]
        C [label="3. Submit patch"]
        CA [label="3. Submit patch"]
        CB [label="3. Submit patch"]
        D [label="4. Comunity
        consultation"]
        E [label="5. Approve change"]
        F [label="6. Increment version"]
        G [label="7. Release new
        version"]
        A -> B -> C -> D -> E -> F -> G
        A -> BA -> CA -> D
        A -> BB -> CB -> D

        lane {
           label = "Submitter"
           A
           B
           C
        }
        lane {
          label = "Karaage community"
           BA
           CA
          D
        }
        lane {
           label = "Karaage team"
           BB
           CB
           E
           F
           G
        }
    }


Submit request
~~~~~~~~~~~~~~
An issue can be opened in the github issue tracker for karaage. The reflects
the fact that this feature is desired, and if it is being worked on, and what
the current status is. This issue should constantly be updated to reflect the
current station of the change.

Modify SRS
~~~~~~~~~~
Modify the text to reflect the desired change. Only the bare minimum
required to address the concern should be changed, if unrelated changes
are required, these should be submitted as separate patches.

Submit patch
~~~~~~~~~~~~
Changes can be submitted as patches to our Gerrit system.

Community Consultation
~~~~~~~~~~~~~~~~~~~~~~
The community consultation will only be used in cases where the proposed change
has wider consequences that could affect other Karaage users, at the discretion
of the Karaage maintenance team.

Approve change
~~~~~~~~~~~~~~
We will aim to accept changes to the SRS, in approximate order of priority:

*   Security issues.
*   Minor mistakes, spelling mistakes, that do not change the meaning of the
    document, will be incorporated ASAP.
*   Any changes to correct ambiguous wording of the document should be
    discussed with the Karaage community first.
*   Changes that don't break existing installs.
*   Changes that don't require database migrations.

Changes that break existing installs or require database migrations will
require:

*   Modification not to do this. Or:
*   Be scheduled for the next major release, and contain appropriate
    documentation and/or migrations to handle upgrades automatically.

Increment version
~~~~~~~~~~~~~~~~~
SRS version numbers are composed of three integers: major.minor.patch:

*   *major*: indicates a major release of SRS. Such changes may have
    incompatible changes with code that complies with previous versions. After
    a new major release, the previous major version will continue to be
    supported and bugs fixed.

*   *minor*: a change in the minor version indicates significant, but not
    major, changes, e.g. database migrations and/or template changes may be
    required in the upgrade. The old version will no longer be supported.
    Installations that comply with the old specification will still comply
    with this specification.

*   *patch*: indicates bug fixes and/or other small changes. Could include
    involve fixing security issues. The old version will no longer be
    supported, and should not be used any more.  Installations that comply with
    the old specification will still comply with this specification.

    Rarely, it is possible that fixing security issues may unavoidably break
    existing code.  This breakage, if required,  will be kept to an absolute
    minimum.

Release new version
~~~~~~~~~~~~~~~~~~~
New patch releases of SRS are released most frequently. They are released
as required, depending on how important the changes are, and if it fixes
security issues.

New minor releases of SRS are released according to demand, how important
the changes are, and if it fixes security issues. The aim is to release these
not more then one a month.

New major releases of SRS will be made as required, but not before V3 has
upgraded its SRS installation to at least the previous major release. The
aim is not to release more then one major release a year.

Any pending requests resolved can now be closed.


Karaage change requirements
---------------------------
This section documents to requirements for generating new versions of Karaage.

Features requests that do not comply with these specifications will not be
considered unless the specifications are updated first.

Submitting patches that meet our submission guidelines will increase the
priority of the feature being incorporated.

..  actdiag::
    :maxwidth: 520

    actdiag {
        A [label="1. Submit request"]
        B [label="2. Modify Karaage"]
        BB [label="2. Modify Karaage"]
        BA [label="2. Modify Karaage"]
        C [label="3. Submit patch"]
        CA [label="3. Submit patch"]
        CB [label="3. Submit patch"]
        D [label="4. Comunity
        consultation"]
        E [label="5. Approve change"]
        F [label="6. Increment version"]
        G [label="7. Release new
        version"]
        A -> B -> C -> D -> E -> F -> G
        A -> BA -> CA -> D
        A -> BB -> CB -> D

        lane {
           label = "Submitter"
           A
           B
           C
        }
        lane {
          label = "Karaage community"
           BA
           CA
          D
        }
        lane {
           label = "Karaage team"
           BB
           CB
           E
           F
           G
        }
    }


Submit request
~~~~~~~~~~~~~~
An issue can be opened in the github issue tracker. The reflects the fact that
this feature is desired, and if it is being worked on, and what the current
status is. This issue should constantly be updated to reflect the current
station of the change.

Modify Karaage
~~~~~~~~~~~~~~
Modify Karaage to reflect the desired change. Only the bare minimum required to
address the concern should be changed, if unrelated changes are required, these
should be submitted as separate patches.

Submit patch
~~~~~~~~~~~~
Changes can be submitted as patches to our gerrit system.

Community Consultation
~~~~~~~~~~~~~~~~~~~~~~
The community consultation will only be used in cases where the proposed change
has wider consequences that could affect other Karaage users, at the discretion
of the Karaage maintenance team.

Approve change
~~~~~~~~~~~~~~
We will aim to accept changes to Karaage, in approximate order of priority:

*   Security issues.
*   Additions/Changes to tests.
*   Minor bug fixes.
*   Changes that don't require database migrations or break existing
    installations.
*   Changes that don't break existing installations.
*   Other changes.

Changes that do not comply with the current version of the SRS in use will not
be accepted, unless the change addresses a security issue.

Increment version
~~~~~~~~~~~~~~~~~
Karaage version numbers are composed of three integers: major.minor.patch:

*   *major*: indicates a major release of Karaage. A major release can comply
    with a new major release of the SRS.

    Such changes may have incompatible changes with previous releases. After a
    new major release, the previous version will continue to be supported and
    bugs fixed. Support for upgrading may not be supported for more then one
    major release at a time.  For example, version 1 users may have to upgrade
    to version 2 before upgrading to version 3. Upgrading to a major

    If there is a major release of Karaage without a corresponding major
    release of the SRS, this would suggest that the SRS has not covered areas
    that are required, as any incompatible changes should be be covered in the
    specifications.

    After a major release, Karaage will no longer comply with the previous
    release of the SRS.

*   *minor*: a change in the minor version indicates significant, but not
    major, changes. A minor release can comply with a new minor release or
    patch release of the SRS.

    For example, database migrations, may be involved in the upgrade. The old
    version will no longer be supported, however there shouldn't be any issues
    in upgrading.  Upgrading to a new minor release may require small amounts
    of downtime to do database migrations and/or update configuration.

    If there is a minor release of Karaage without a corresponding minor
    release of the policy, this would typically suggest that internal
    changes were made that could affect deployment, and don't need to
    be specified.

    After a minor release, Karaage will continue to comply with the
    previous version of the SRS, as a minor update to the SRS means
    compability should be preserved.

*   *patch*: indicates bug fixes and/or other small changes. A patch release
    could comply with a new patch release of the SRS.

    Some changes could involve fixing security issues. The old version will no
    longer supported, and should not be used any more. No changes should be
    required other then upgrading the package.

    Rarely, it is possible that fixing security issues may unavoidably break
    existing code.  This breakage, if required, will be kept to an absolute
    minimum.

    After a path release, Karaage will continue to comply with the previous
    version of the SRS, as a patch update to the SRS means compability should
    be preserved (not counting security issues).

Every release of Karaage will be documented as complying with version X.Y.Z of
the SRS.

Release new version
~~~~~~~~~~~~~~~~~~~
New patch releases of Karaage are released most frequently. They are released
as required, depending on how important the changes are, and if it fixes
security issues.

New minor releases of Karaage are released according to demand, how important
the changes are, and if it fixes security issues. The aim is to release these
not more then one a month.

New major releases of Karaage will be made as required, but not before V3 has
upgraded its Karaage installation to at least the previous major release. The
aim is not to release more then one major release a year.

A best effort will be made to keep up with the latest version of the SRS at all
times, within the requirements specified here.
