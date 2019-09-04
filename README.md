Mongo dump
==========

This playbook will dump a mongo database in a folder and delete dumps older than 7 days if prune is set to yes. Works for debian only.

Usage example
-------------

### With ansible

```bash
ansible-playbook /var/www/ansible/playbooks/mongo-dump/main.yml \
    -e "mongo_dumps_target_folder=/var/folder/mongo_dumps" \
    -e "prune=yes" \
    -e "db_host=mongo.domain.org" \
    -e "db_port=27017" \
    -e "db_name=mongo_db_name" \
```

### Using the ansible docker image with the docker-compose configuration

Update the `docker-compose.yml` file according to your needs, then run:

```
docker-compose run mongo-dump
```
