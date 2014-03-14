Future directions
=================
*   Only administrators can access usage information unless Karaage is
    configured to allow public access to it. This may be a regression from
    Karaage 2. See the :ref:`additional_access_people`,
    :ref:`additional_access_projects`, and 
    :ref:`additional_access_institutes` sections.

*   More roles are needed at some sites to enable some users to have increased
    access to data. See the :ref:`roles` section.

*   It is common practise to copy files to create local customizations of
    Karaage.  This breaks upgrades.

*   RPC needs fixing. Not all sites require it, and not consistent. Possible
    things to change include:

    *   Possible to disable it if not required?
    *   Replace with modern REST API?
    *   Remove it?
    *   All methods require authentication?

*   The implemented change_default_project RPC specification is broken. There
    is no indication of which account it should operate on. Is it needed?

    ..  py:function:: change_default_project(username, password, pid)

        :param str username: Authenticate as this person.
        :param str password: Person's password.
        :param str pid: PID of new project to use as default.
        :return:
            On success, return a tuple (0, str)

            On error, return a tuple (code, string)
        :rtype: tuple

        Change the default project for the person's account identified by
        account_username.

