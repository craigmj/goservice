goservice
========

Fetches a go repo, builds it, and installs an upstart job to start the service.

Requirements
------------

None.

Role Variables
--------------

*repo*
The repo of the go app.

*name*
The name of the app and the associated upstart job. The repo will be checked out into {{path}}/{{name}}

*path*
The path where the repo should be fetched to.

*vcs*
'git' by default, but can be set to 'hg' for using mercurial.

Dependencies
------------

Require go on the system.

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: proxy
      roles:
         - role: craigmj.goservice
           repo: https://github.com/craigmj/mygowebserver.git
           name: mygowebserver
           path: /opt/github.com/craigmj

License
-------

BSD

Author Information
------------------
