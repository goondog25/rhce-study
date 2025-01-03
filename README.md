# RHCE Study Preparation

## Study Resources
1. [Oreilly Learning Video Course by Sander Van Vugt](https://learning.oreilly.com/course/red-hat-certified/9780138271657/)
2. [Book: RHCE Cert Guide by Sander Van Vugt](https://www.amazon.com/RHCE-EX294-Cert-Guide-Certification/dp/0136872433/ref=sr_1_1?crid=1PMQZIG6VF33W&dib=eyJ2IjoiMSJ9.i-ddoTpDl9FtL3_grGGJeWUfBjh3voBjqLWIjzLKC0LOqHzPpiQlx4slPo0xcmem8WevdGE28-Y3z2xkbgjIpUy4PNrQ3pKMV_yfGWw0lRvYS9w8BOZuUC2O_xHFzVjEOYEyKqSSkrsyCSYXsFUPocSVFwDD4vqIDHIW67oNQRnktjAYaqh-tLjHG4X2gOk88YZ1YJZ3k3LNyLzSwIhskbZEJYRonW68s4zipIVuh3M.liFqReEhyPqEUw4Ld1ZPWLcza_3r-69w_NoiFKIxKpg&dib_tag=se&keywords=rhce&qid=1735921291&sprefix=rhce%2Caps%2C118&sr=8-1)
3. [Book: Ansible for DevOps by Jeff Geerling](https://www.amazon.com/Ansible-DevOps-Server-configuration-management/dp/0986393428/ref=sr_1_1?crid=AR9GPJA231YL&dib=eyJ2IjoiMSJ9.fr28Fsuo5NFB_CYLAY8cCFo6dV0UuEX-ubHbBWIASdXJC7BY98s9YC9-ySzuDj2rE3fkvM7dU7Xc1FCBu1_1B89gwHh7vVEjDjmjw-BUCRF9woKnznxpb2SI7lyBJtYdzJ57Up_UN2Tnc6rGrFLfeBBxCirwJfTjL3UNpoCea0jJ14xCW8je9GA98925qvuec96HZH7L-FOzbnJ9k_qMMfBjo2oXMRcyPX-4RK5HhAg.fatnYls4R1A5P0eG4XenEGbVbfhPik5hqYPywmFtM08&dib_tag=se&keywords=ansible+for+devops&qid=1735921469&sprefix=ansile+for+d%2Caps%2C128&sr=8-1)

## Important Ansible Modules

### General Purpose
1. `raw` - Straight up ssh commands when python unavailable on managed node.
2. `command` - Execute singular commands on remote system
3. `shell` - Excute commands with the shell environment of the remote system

### Software Packages and Repositories
4. `ansible.builtin.yum`: Manage packages with `yum` or `dnf`.
5. `ansible.builtin.yum_repository`: Manage repository configurations.
6. `ansible.builtin.package`: Generic package management module (can use yum as the backend).

### Services
7. `ansible.builtin.service`: Manage services using init or systemd.
8. `ansible.builtin.systemd`: Manage services directly with systemd on RHEL systems.

### Firewall Rules
9. `ansible.posix.firewalld`: Manage `firewalld` services and rules.
10. `ansible.builtin.iptables`: Manage `iptables` firewall rules.

### File Systems
11. `ansible.builtin.mount`: Mount and unmount file systems.
12. `ansible.builtin.filesystem`: Create, resize, and delete file systems.

### Storage Devices
13. `ansible.builtin.lvg`: Manage LVM volume groups.
14. `ansible.builtin.lvol`: Manage LVM logical volumes.
15. `ansible.builtin.parted`: Manage partition tables.

### File Content
16. `ansible.builtin.lineinfile`: Manage lines in text files.
17. `ansible.builtin.blockinfile`: Insert/update blocks of text in files
18. `ansible.builtin.copy`: Copy files to remote hosts.
19. `ansible.builtin.template`: Deploy templates to hosts.
20. `ansible.builtin.replace`: Replace specific text in a file.

### Archiving
21. `ansible.builtin.unarchive`: Extract archives on remote machines.
22. `ansible.builtin.archive`: Create tarball archives.

### Task Scheduling
23. `ansible.builtin.cron`: Manage cron jobs.
24. `ansible.builtin.at`: Schedule one-time tasks using the at command.

### Security
25. `ansible.posix.seboolean`: Manage SELinux booleans.
26. `ansible.posix.selinux`: Toggle the SELinux policy state.
27. `ansible.posix.auditd`: Manage auditd rules.
28. `ansible.posix.pam_limits`: Manage PAM limits for users and groups.

### Users and Groups
29. `ansible.builtin.user`: Manage local users.
30. `ansible.builtin.group`: Manage local groups.
31. `ansible.builtin.authorized_key`: Manage SSH authorized keys for users.


## RHCE Exam Objectives

### Be able to perform all tasks expected of a Red Hat Certified System Administrator

- Understand and use essential tools
- Operate running systems
- Configure local storage
- Create and configure file systems
- Deploy, configure, and maintain systems
- Manage users and groups
- Manage security

### Understand core components of Ansible

- Inventories
- Modules
- Variables
- Facts
- Loops
- Conditional tasks
- Plays
- Handling task failure
- Playbooks
- Configuration files
- Roles
- Use provided documentation to look up specific information about Ansible modules and commands

### Use roles and Ansible Content Collections

- Create and work with roles
- Install roles and use them in playbooks
- Install Content Collections and use them in playbooks
- Obtain a set of related roles, supplementary modules, and other content from content collections, and use them in a playbook.

### Install and configure an Ansible control node

- Install required packages
- Create a static host inventory file
- Create a configuration file
- Create and use static inventories to define groups of hosts

### Configure Ansible managed nodes

- Create and distribute SSH keys to managed nodes
- Configure privilege escalation on managed nodes
- Deploy files to managed nodes
- Be able to analyze simple shell scripts and convert them to playbooks

### Run playbooks with Automation content navigator
- Know how to run playbooks with Automation content navigator
- Use Automation content navigator to find new modules in available Ansible Content Collections and use them
- Use Automation content navigator to create inventories and configure the Ansible environment

### Create Ansible plays and playbooks
- Know how to work with commonly used Ansible modules
- Use variables to retrieve the results of running a command
- Use conditionals to control play execution
- Configure error handling
- Create playbooks to configure systems to a specified state

### Automate standard RHCSA tasks using Ansible modules that work with:
- Software packages and repositories
- Services
- Firewall rules
- File systems
- Storage devices
- File content
- Archiving
- Task scheduling
- Security
- Users and groups

### Manage content

- Create and use templates to create customized configuration files
- Use Ansible Vault in playbooks to protect sensitive data
