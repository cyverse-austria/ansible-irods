# ansible-irods

Installing iRODS `4.3.1` on Ubuntu `22.04`


## run playbooks
```bash
# install requirements
ansible-galaxy install -r .yml

ansible-playbook --inventory $INVENTORY_DIR/ --user=root playbooks/irods/provision_irods.yml
```


## resource server
* ./irodsctl start - failing is ok
* sed -i '/"previous_version": {/,/}/d' /var/lib/irods/version.json
* iinit 
* ./irodsctl start
* iinit
* ./irodsctl restart
