# Setup PC with Ansible

Ansible playbooks to setup my PC for software development. Latest Ubuntu/Debian only. 

# Requirements

To install ansible in a python virtual environment, first install python3-venv.

```
sudo apt-get install python3-venv
```
Afterwards create and activate the python virtual environment with:

```
cd ~ 
python -m venv devops
source ~/devops/bin/activate
```

Then install ansible:

```
python -m pip install ansible
```

Then download this repo and unarchive in your desired directory.

Install third-party roles/collections before executing any playbooks:

```
ansible-galaxy install -r ./requirements.yml
```


# Execute Playbooks

Either execute the *main.yml* playbook or execute a specific playbook inside the *playbooks* directory.

```
ansible-playbook --ask-become-pass ./main.yml
```

You will be asked to enter the sudo password of the user specified in the group_vars all.yml file.
