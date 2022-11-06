# Ansible-MariaDB
This ansible playbook automates the installation of MariaDB on a Centos 7 instance.

## Prerequisites
- Ansible
- Centos 7 instance

## Usage
- Clone the repository
```	
git clone https://github.com/the-src/Ansible-MariaDB.git
```
- Edit the `hosts` file to include the IP address of the Centos 7 instance
```
echo -e "[databases]\n<IP_ADDRESS> ansible_ssh_user:<USERNAME> ansible_ssh_pass:<PASSWORD>" > hosts
```
- Run the playbook using the command `ansible-playbook -i hosts mariadb.yml`
- The playbook will install MariaDB and start the service
- The playbook will also create a database called `internship` with the following schema:
```sql
CREATE TABLE `interviews` (
id int not null auto_increment,
name varchar(255),
primary key (id)
);
```