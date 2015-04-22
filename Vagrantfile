# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "chef/centos-6.6"
  
  config.vm.provision "shell", inline: "sudo yum install libselinux-python -y"
  

  config.vm.define "host1" do |host1|
    host1.vm.network "private_network", ip: "192.168.33.20"
  end

  config.vm.define "host2" do |host2|
    host2.vm.network "private_network", ip: "192.168.33.21"
  end
  
  
  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end
  
  
end
