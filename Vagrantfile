# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-22.04"
  #Use this if the subnet is 192.168.1.0
  config.vm.network "public_network", ip: "192.168.1.55" #Use this if the subnet is 192.168.1.0
  #config.vm.network "private_network", ip: "192.168.1.55" #Use this if the subnet isnt 192.168.1.0
  config.vm.provider "virtualbox" do |vb|
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.network "forwarded_port", guest: 9000, host: 9000
config.vm.network "forwarded_port", guest: 4200, host: 4200
config.vm.network "forwarded_port", guest: 3000, host: 3000
config.vm.network "forwarded_port", guest: 9090, host: 9090
  vb.memory = "8192"
  vb.cpus = "4"
end

   config.vm.provision "shell", inline: <<-SHELL
     sudo apt-get -y update
   SHELL
end
