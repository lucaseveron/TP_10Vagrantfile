# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "argocd"
  config.vm.define "argocd"
  config.vm.network "public_network"
  config.vm.network "private_network", ip: "192.168.33.13"
  config.vm.network "forwarded_port", guest: 8080, host: 8080  
#  config.vm.network "forwarded_port", guest: 80, host: 80
#  config.vm.network "forwarded_port", guest: 443, host: 443
  config.vm.provider "virtualbox" do |vb|
    vb.name = "argocd"
    vb.memory = "4096"
    vb.cpus = 2
  end
  config.vm.provision "shell" do |s|
   s.path = 'install.sh' 
   
  end
end