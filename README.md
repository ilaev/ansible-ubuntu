# Setup PC with Ansible

Ansible playbooks to setup my PC for software development. Latest Ubuntu/Debian only.

# Requirements

Ubuntu 26:
> export ANSIBLE_BECOME_EXE=sudo.ws
Because sudo-rs (rewrite in rust and ansible have some issues)

Enter the development shell which provides Python, Ansible, and other tools:

```
cd /path/to/ansible-ubuntu
devenv shell
```

Then install third-party roles/collections before executing any playbooks:

```
ansible-galaxy install -r ./requirements.yml
```

# Execute Playbooks

Either execute the *main.yml* playbook or execute a specific playbook inside the *playbooks* directory.

```
ansible-playbook --ask-become-pass --ask-vault-pass ./main.yml
```

You will be asked to enter the sudo password of the user specified in the group_vars all.yml file.
