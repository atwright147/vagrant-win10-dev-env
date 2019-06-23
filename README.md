# Vagrant Windows 10 Development Environment

## Getting started

### Vagrant

1. Install VirtualBox and Vagrant
    ```sh
    brew install virtualbox vagrant
    ```
1. Clone this repo into a folder
1. Start up the server with Vagrant and ssh into it:
    ```sh
    vagrant up
    ```

### Viewing the DB structure and content

Ansible is used to provision your Windows box, so please ensure that Ansible is installed on your host machine.

#### Install Ansible

```sh
sudo pip install ansible
```

#### Update Ansible

```sh
sudo pip install ansible --upgrade
```

## Notes


