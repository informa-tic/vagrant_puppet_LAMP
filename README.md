#  Creación de un entorno de desarrolo LAMP con Vagrant y Puppet

## Descarga e instalación

[Descargar Vagrant](https://www.vagrantup.com/downloads.html)

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

Creamos el siguiente jerarquía
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
