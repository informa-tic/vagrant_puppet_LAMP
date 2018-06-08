#  Setup Vagrant y Puppet en SO Ubuntu 16.04

## Pre -requisitos

Tener Vagrant y VirtualBox descargados

#### [Descargar Vagrant](https://www.vagrantup.com/downloads.html)

`$ wget https://releases.hashicorp.com/vagrant/1.9.1/vagrant_1.9.1_x86_64.deb`

`$ sudo dpkg -i vagrant vagrant_1.9.1_x86_64.deb`

`$ vagrant -v`

#### [Descargar VirtualBox](https://www.virtualbox.org/wiki/)

## Ejecutar repositorio

`$ vagrant up [vm-name]`

`$ vagrant up initial_env`

`$ vagrant ssh initial_env`

En caso de presentar problemas por falta de compatibilidad entre Vagrant y VirtualBox realizar siguiente configuración manualmente

https://github.com/hashicorp/vagrant/commit/7d73af5637de41f1e53b8f1ef2ea9baf76842dfb

## Apuntes varios

[Ver todos los Comandos (CLI) disponibles](https://www.vagrantup.com/docs/cli)

#### Uninstall Vagrant

`sudo dpkg -r vagrant`

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
