#  SetUp entorno de desarrolo LAMP con Vagrant y Puppet

## Descarga e instalación en SO Ubuntu 16.04

[Descargar Vagrant](https://www.vagrantup.com/downloads.html)

`$ wget https://releases.hashicorp.com/vagrant/1.9.1/vagrant_1.9.1_x86_64.deb`

`$ sudo dpkg -i vagrant vagrant_1.9.1_x86_64.deb`

`$ vagrant -v`

Uninstall Vagrant

`sudo dpkg -r vagrant`

Para desisntallar Vagrant

[Descargar VirtualBox](https://www.virtualbox.org/wiki/)

## Comandos útiles Vagrant

`$ vagrant init`

`$ vagrant box list`

`$ vagrant up [vm-name]`

`$ vagrant up [vm-name] --provision`

`$ vagrant reload [name|id]`

`$ vagrant halt [name|id]`

[Ver todos los Comandos (CLI) disponibles](https://www.vagrantup.com/docs/cli)


## Configuración de Puppet

Creamos la siguiente jerarquía

~~~ 
- puppet
    - manifests
        - default.pp
    - modules
        - mysql
            - files
                - index.php
                - mysql.conf
            - manifests
                - init.php
- VagrantFile 
~~~
