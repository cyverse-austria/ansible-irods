# ansible-irods

Installing iRODS `4.3.1` on Ubuntu `22.04`


## run playbooks
```bash
# install requirements
ansible-galaxy install -r requirements.yml
ansible-galaxy install --force -r collections.yml

ansible-playbook --inventory $INVENTORY_DIR/ --user=root playbooks/irods/provision_irods.yml
```


## resource server

* ./irodsctl start - failing is ok
* sed -i '/"previous_version": {/,/}/d' /var/lib/irods/version.json
* iinit 
* ./irodsctl start
* iinit
* ./irodsctl restart



## error on created user

**After register a new user in data you get**

```bash
Error Code= ERR_ILLEGAL_ARGUMENT
Reason = "java.lang.IllegalArgumentException: Invalid UUID string: "
User = newadmin
```
