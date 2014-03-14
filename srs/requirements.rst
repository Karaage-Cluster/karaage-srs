Specific Requirements
=====================
This section contains all of the functional and quality requirements of the
system. It gives a detailed description of the system and all its features.


External interface requirements
-------------------------------
This section provides a detailed description of all inputs into and outputs
from the system.

User Interface
^^^^^^^^^^^^^^
Karaage is web based, so it is expected most :term:`users` will access it via a
web browser loaded on their computer.

The user interface should ibe easy, simple, and obvious to use for
all target users of karaage, as per :ref:`user_characteristics`.

Software Interfaces
^^^^^^^^^^^^^^^^^^^
Karaage needs access to external :term:`data stores`, which at present time
consists one/more of:

*   OpenLDAP
*   Directory Server/389
*   Slurm
*   Gold

.. todo:

    *   Active Directory

Other datastores to be provided by third party software, e.g. karaage-keystore.

An API is required for use by submission scripts used by the PBS software, to
retrieve information required for the submission. This API is only required if
PBS software is used.

An API is also required to submit :term:`super computer` usage information,
if required by :term:`local requirements`.

Functional requirements
-----------------------
This section includes the requirements that specify all the fundamental actions
of the software system.

.. _operating_system_requirements:

Operating system requirements
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The servers used for Karaage should be able to run on Debian Wheezy, using
using the Python 2.7 language.

A Mysql database is required for storing Karaage data.

.. todo:

    RHEL6 support.

Role requirements
^^^^^^^^^^^^^^^^^
Users can use karaage as different roles. The following roles are
defined:

*   :term:`Unauthenticated users`
*   :term:`People`
*   :term:`Project leaders`
*   :term:`Institute delegates`
*   :term:`Administrators`

Access requirements
^^^^^^^^^^^^^^^^^^^
Different roles have access to different sets of functions.

:term:`Unauthenticated users`:

*   Apply for an account
*   Login

:term:`People`:

*   View details for own person.
*   View details for people in own projects.
*   View details for projects they belong to.
*   View details for machines and machine categories.
*   View details for software.
*   View usage information (optional).
*   Agree to licensed software.
*   Apply for restricted software.
*   Modify their own person.
*   Change password.
*   Reset password.
*   Logout

:term:`Project leaders`:

*   View details for people in project they lead.
*   View details for projects that they lead
*   Approve/Decline applications to join their project.
*   Reset passwords for their members.
*   Track their resource utilisation and software utilisation.
*   Edit project (restricted set of fields).

:term:`Institute delegates`:

*   View details for people in institute they delegate.
*   View details for people in project for institute they delegate.
*   View details for projects for institute they delegate.
*   View details for institutes they delegate.
*   Approve/Decline project applications.
*   Manage all projects and users under the institute.

:term:`Administrators`:

*   View/edit details for people.
*   View/edit details for projects.
*   View/edit details for institutes.
*   View/edit details for machine and machine categories.
*   View/edit details for software.
*   View usage information.
*   Change passwords for any person.
*   Creating/delete/reactivate people [#delperson]_.
*   Creating/delete accounts [#delaccount]_.
*   Creating/delete projects.
*   Creating/delete institutes.
*   Approve/Decline project applications.
*   Approve/Decline software applications.
*   Lock/unlock people.
*   Make person as bounced email.
*   View logs/comments for any object.
*   Add comments to any object.
*   View low level (verbose) information from datastores.

.. _additional_access_requirements:

Additional Access requirements
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Having access to view details for a person implies being able to:

*   Send email allowing person to reset their passwords
*   View list of all projects person leads.
*   View list of all projects person belongs to.
*   View list of all software agreements.
*   View list of all accounts for person.
*   View list of all jobs for person.

Having access to view details for a project implies being able to:

*   View project caps/quota for project.
*   View list of members of project.
*   View list of projects in institute.
*   View usage information for the project [broken].

Having access to view details for institutes implies being able to:

*   View project caps/quota for institute.
*   View list of members of institute.
*   View usage information for the institute [broken].
*   View the insitute users information for the institute.


.. _performance_requirements:

Performance requirements
------------------------
The requirements in this section provide a detailed specification of the user
interaction with the software and measurements placed on the system
performance.


Design constraints
------------------
This section includes the design constraints on the software caused by the
hardware.

As Karaage is a software project, this is outside the scope, and needs to be
set in a project plan for installing Karaage at a particular site.

Any reliable computer that meets the :ref:`operating_system_requirements` and
can function as a webserver that meets the :ref:`performance_requirements`
should be suitable for use with Karaage.


Software System attributes
--------------------------
The requirements in this section specify the required reliability,
availability, security and maintainability of the software system.

As Karaage is a software project, this is outside the scope, and needs to be
set in a project plan for installing Karaage at a particular site.


Other requirements
------------------

..  rubric:: Footnotes

..  [#delperson] People are never deleted, rather the db entry is marked
    as deleted. This is to ensure usernames are never recycled.

..  [#delaccount] Accounts are never deleted, rather the db entry is marked
    as deleted. This is to ensure usernames are never recycled.
