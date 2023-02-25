mail_after_reboot_service
=========

Create and enable a systemd service that sends an e-mail after the host has been rebooted (needs an installed MTA like postfix...)

Requirements
------------

None.

Role Variables
--------------

`mail_recipient`: Recipient of the mail, default value is `root`.
`mail_executable`: Executable to send the mail, defaults to `/usr/bin/mail` (or `/usr/bin/s-nail` on Debian).
`dependency`: Which other systemd service the mail_after_reboot.service should depend on (and wait for), defaults to `postfix.service`.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: 'ojkastl.mail_after_reboot_service' }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via mail@ojkastl.de or kastl@b1-systems.de.
