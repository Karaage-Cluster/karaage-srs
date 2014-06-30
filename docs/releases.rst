Prioritization and Release Plan
===============================
This discusses topics associated with new releases of Karaage and feature
requests.

Enhancements
------------
Any small changes or bug reports, that don't require changes to these
specificiations, should be submitted to the `github issue tracker
<https://github.com/Karaage-Cluster/karaage/issues/>`_. Even better, changes
can be submitted to our `gerrit <https://code.vpac.org/gerrit/>`_.

More significant changes may require creating a KEP (Karaage Enchangement
Proposal). See `KEP 1: KEP Purpose and Guidelines
<https://github.com/Karaage-Cluster/keps/blob/master/keps/0001.rst>`_ for
details.

Any KEP should consider if it requires changes to these specifications,
and the release requirements mentioned in this section.

The process of creating a KEP involves community consultation.

Karaage release requirements
---------------------------
This discusses the requirements for making a new Karaage release.

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
