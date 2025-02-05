# ansible-irods

Installing iRODS `4.3.1` on Ubuntu `22.04`


## run playbooks
```bash
# install requirements
ansible-galaxy install -r .yml

ansible-playbook --inventory $INVENTORY_DIR/ --user=root playbooks/irods/provision_irods.yml
```


