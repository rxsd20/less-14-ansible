# -*- mode: ruby -*-
# vi: set ft=ruby :
   
Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu1804"
  config.vm.network "private_network", ip: "192.168.121.240"
  config.vm.provider "libvirt" do |v|
    v.memory = 1512
    v.cpus = 2
  end
  config.vm.hostname = "nginx-vm"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "start_nginx.yml"
  end
end
