Glossary
========

..  glossary::
    :sorted:

    user
    users
        A :term:`person` who is currently using Karaage.

    unauthenticated user
    unauthenticated users
        Somebody who is currently using Karaage, who has not authenticated to
        Karaage, and may not even be a :term:`person`.

    :index:`person <role;person>`
    people
        A person who has access to the Karaage system. A person could have
        one/more accounts, be an administrator, be a project manager, be an
        institute delegate. These are optional.

    machine
        A single cluster or computer which is managed as a distinct unit.

    machine category
        A group of machines that share the same authentication systems.

    data store
    data stores
        A list of external databases that we should link to and update
        automatically.  Supported databases include LDAP, Gold, and Slurm.

    account
        A person may have one or more accounts. An account allows a person to
        access machines on a given machine_category. A person needs to belong
        to a :term:`project` to have an account, although there may be specific
        exceptions to this rule.

    group
        A list of people. Usually maps directly to an LDAP Group, but this
        depends on the data stores used.

    project
        A list of people who share the common goal.

    :index:`project leader <role;project leader>`
    project leaders
        A person who manages a project, and can allow new user's to use the
        project.

    institute
        An Institute is just a group of projects.

    :index:`institute delegate <role;institute delegate>`
    institute delegates
        A person who manages an institute, and can allow new project's for the
        institute.

    :index:`administrator <role;administrator>`
    administrators
        A person who has unlimited access to Karaage.

    local installation
        A custom installation of Karaage at a particular site for a particular
        purpose.

    local requirements
        Any requirements that are specific to a local installation.

    super computer
        A computer system with that :term:`people` can use and submit jobs on.
