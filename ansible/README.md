# README

This `ansible-playbook` intend to configure a `k3s` cluster running on `raspberry-pi` boards.

It leverage `docker` to minimize local dependencies.

## Pre-requisites

* `docker`
* password-less `ssh` connection to all the `raspberry-pi`

## HOW TO

```
# adjust 'inventory/' as needed
./ansible-playbook -i ./inventory setup.yml
```
