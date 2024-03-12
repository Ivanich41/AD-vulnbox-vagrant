# -*- mode: ruby -*-
# vi: set ft=ruby :

# ARM Vmware 

Vagrant.configure("2") do |config|

    config.vm.box = "spox/ubuntu-arm"
  
    config.vm.provider :vmware_desktop do |vmware|

        vmware.gui = true
        vmware.cpus = 4
        vmware.memory = 4096
        vmware.vmx["ethernet0.virtualdev"] = "vmxnet3"
        vmware.ssh_info_public = true
        vmware.linked_clone = false

    end
  
    config.vm.hostname = "ad-vulnbox"
    config.vm.synced_folder ".", "/vagrant"
    
    config.vm.provision "ansible_local" do |ansible|
      ansible.install = true
      ansible.verbose = "v"
      ansible.playbook = "provision.yml"
    end
  
end
  