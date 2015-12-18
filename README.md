Role Name
=========

An ansible role for managing NFS mounts. For now this just mounts NFS shares on clients. I hope to add server configuration in the future.


Role Variables
--------------

| Variable				| Default				| Notes					|
| :---					| :---					| :---					|
| nfs_server_install			| false					| 					|
| nfs_client_install			| true					|					|
| nfs_mounts				| []					|					|

  nfs_mounts:
    - server: x.x.x.x
      export_name: /data
      mount_point: /mnt/nfs

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: correcthorse.nfs }

License
-------

MIT

Author Information
------------------

* [Joshua Rusch](https://correct.horse/)
