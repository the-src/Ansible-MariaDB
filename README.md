# Ansible-MariaDB
This ansible playbook automates the installation of MariaDB on a Centos 7 instance.

## Prerequisites
- Ansible
- Centos 7 instance

## Usage
- Clone the repository
- Edit the `hosts` file to include the IP address of the Centos 7 instance
- Run the playbook using the command `ansible-playbook -i hosts mariadb.yml`
- The playbook will install MariaDB and start the service
- The playbook will also create a database called `internship` with the following schema:
```
CREATE TABLE `interviews` (
id int not null auto_increment,
name varchar(255),
primary key (id)
);
```