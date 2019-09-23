# RHMI Upgrade 1.5

Quick and simple playbook to automate all the "extra" validation steps or fix known issues as part of the 1.5 upgrade.

## How to use

### Extra variables required to run are:
```
- openshift_console_url
- openshift_token (cluster admin
```

### Requirements
```
pip install -U Jinja2
```

### Example usage
```
# Run backups
ansible-playbook -i test/inventories playbooks/backups.yml -e openshift_console_url=https://console.cake.openshift.com -e openshift_token=ireallylikecake

# Post install
ansible-playbook -i test/inventories playbooks/post_install.yml -e openshift_console_url=https://console.cake.openshift.com -e openshift_token=ireallylikecake

```
