# -*- mode: ruby -*-
# vi: set ft=ruby :

# x86 Virtualbox

Vagrant.configure("2") do |config|

  config.vm.box = "generic/debian12"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "ad-vulnbox"
    vb.memory = "4096"
    vb.cpus = 4
#   # Display the VirtualBox GUI when booting the machine
    # vb.gui = true
  end

  config.vm.hostname = "ad-vulnbox"
  config.vm.synced_folder ".", "/vagrant"
  config.vm.network "private_network", ip: "192.168.228.100", :adapater=>2

  config.vm.provision "ansible_local" do |ansible|
    ansible.install = true
    ansible.verbose = "v"
    ansible.playbook = "provision.yml"
  end

end
