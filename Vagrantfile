# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  # Sistema operativo
  config.vm.box = 'ubuntu/trusty64'

  # IP privada
  config.vm.network 'private_network' ip: '192.168.33.10'

  config.vm.provider :virtualbox do |vb|

      #Nombre de la máquina virtual
      vb.name = 'lamp'

      # Memoria
      vb.memory = '2048'

      # Número de procesadores
      vp.cpus = 2
  end

  #Habilitamos Puppet como aprovisionamiento
  config.vm.provision :puppet do |puppet|

    #Path de los ficheros de configuración
    puppet.manifests_path = 'puppet/manifests'

    #Nombre del manifiesto que se va ejecutar primero
    puppet.manifests_file = 'default.pp'

    #Opciones de puppet. Aactivamos modo debus y verbose
    puppet.options = [
      '--verbose',
      '--debug',
    ]
  end
end
