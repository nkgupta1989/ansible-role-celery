# Community Platform Deployment

#### Celery

`run_celery_beat`

* This host will run celery beat
* Should run on only one host


## Setup

### Install ansible client

##### On mac

	brew install ansible

##### On Ubuntu

	sudo apt-get install ansible

### To fix the root user on ec2 boxes

	ansible-playbook -i digital ec2.yml

### To ensure root can access servers

	ansible -vv -i development all -u root -m ping

### To configure servers

	ansible-playbook -i inventories/development site.yml