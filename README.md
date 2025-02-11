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



# TODO

User: newadmin
Pass: mojibwali


    # # TODO: create a task on - irods_runtime_init.yml
    # # create irods account for de-irods
    # iadmin mkuser de-irods rodsadmin
    # iadmin moduser de-irods password kmOdwrybisdRPY1M

    ## add de-irods to the rodsadmin group 
    # iadmin atg rodsadmin de-irods

    # # portal user irods
    # iadmin mkuser portal rodsadmin
    # iadmin moduser portal password ksasagrybisdRPY1M

###########################
    # # rodsadmin should own /TUG/home/shared
    # ichmod own rodsadmin /TUG/home/shared

    # # add this to database deployment
    # \c ICAT
    # GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA "public" TO icat_reader;



## After register a new user in data you get
```bash
Error Code= ERR_ILLEGAL_ARGUMENT
Reason = "java.lang.IllegalArgumentException: Invalid UUID string: "
User = newadmin
```
