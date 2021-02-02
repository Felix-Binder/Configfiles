
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
  config.vm.network "private_network", ip: "192.168.0.10"
  config.vm.hostname  = "localdev"
  config.vm.boot_timeout = 300

  # config.vm.provider "virtualbox" do |vb|
  #   vb.name = "localdev"
  #   vb.memory = "4048"
  #   vb.cpus = 2
  # end

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get upgrade
    sudo apt install software-properties-common
    sudo apt-add-repository --yes --update ppa:ansible/ansible
    sudo apt-get install ansible git nodejs npm
  SHELL
end
