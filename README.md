Role Name
========

Run-Your-Own Firefox Sync Server: https://github.com/mozilla-services/syncserver

Requirements
------------


Role Variables
--------------


Dependencies
------------

Optional:
    - nginx
    - apache/wsgi
    - mysql
    - ...

Example Playbook
-------------------------

    - hosts: mozsync
      roles:
         - role: bennojoy.mysql
         - role: Ginsys.mozsync


Once the server is launched, you need to tell Firefox about its location. Go to
“about:config”, search for “services.sync.tokenServerURI” and change its value
to the URL of your server with a path of “token/1.0/sync/1.5”:

services.sync.tokenServerURI: http://sync.example.com/token/1.0/sync/1.5


License
-------

GPLv3

Author Information
------------------

(c) Serge van Ginderachter <serge@vanginderachter.be>

