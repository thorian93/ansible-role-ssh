# Ansible Role: SSH

This role configures sshd on RHEL/CentOS, Debian/Ubuntu and Fedora servers.

## Requirements

No special requirements; note that this role requires root access, so either run it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

    - hosts: foobar
      roles:
        - role: ansible-role-ssh
          become: yes

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

# Security Server Role Documentation:
The following is a list of currently available variables for the security server role and some example values.

    sshd_port: 22

Configure the port sshd listens on.

    sshd_permit_root_login: "no"

Allow login as root user.

    sshd_permit_password_authentification: "no"

Allow password authentication.

    sshd_strict_mode: "yes"

Use sshd strict mode.

    sshd_allowed_users: []

Allowed users for ssh login. **Currently not implemented!**

    sshd_allowed_groups: "sshlogin"

Allowed groups for ssh login.

    sshd_allow_x11_forwarding: "no"

Allow X11 forwarding.

## Dependencies

None.

## Example Playbook

    - hosts: foobar
      become: yes
      roles:
        - ansible-role-ssh

## Disclaimer

This role is provided AS IS and I can and will not guarantee that the role works as intended, nor can I be accountable for any damage or misconfiguration done by this role. Study the role thoroughly before using it.

## License

GPLv3

## Author Information

This role was created in 2019 by [Thorian93](https://thorian93.de/).
