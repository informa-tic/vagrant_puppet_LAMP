# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Sistema operativo
  config.vm.box = "ubuntu/trusty64"
  #config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  # Definimos configuración llamada test
    config.vm.define "defualt" do |defualt|
    # IP privada
    defualt.vm.network "private_network", ip: "192.168.55.2"
    # Synced folders
    defualt.vm.synced_folder "../", "/src"

    # Habilitamos Puppet como aprovisionamiento
    defualt.vm.provision :puppet do |puppet|
      #Path de los ficheros de configuración
      puppet.manifests_path = "./puppet/manifests"
      # #Direcotrio de los módulos
      # puppet.module_path = "./puppet/modules"
      # #Nombre del manifiesto que se va ejecutar primero
      # puppet.manifests_file = "defualt.pp"
    end

    # Memoria
    defualt.vm.provider "virtualbox" do |vb|
      vb.memory = '2048'
      vb.cpus = 2
    end
   end

  # Definimos configuración llamada test
    config.vm.define "initial_env" do |initial_env|
    # IP privada
    initial_env.vm.network "private_network", ip: "192.168.55.2"
    # Synced folders
    initial_env.vm.synced_folder "../", "/src"

    # Habilitamos Puppet como aprovisionamiento
    initial_env.vm.provision :puppet do |puppet|
      #Path de los ficheros de configuración
      puppet.manifests_path = "./puppet/manifests"
      # #Direcotrio de los módulos
      # puppet.module_path = "./puppet/modules"
      # #Nombre del manifiesto que se va ejecutar primero
      # puppet.manifests_file = "initial_env.pp"
    end

    # Memoria
    initial_env.vm.provider "virtualbox" do |vb|
      vb.memory = '2048'
      vb.cpus = 2
    end
  end
end
