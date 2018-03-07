# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

    # Use the same key for each machine
    config.ssh.insert_key = false
  
    # Create the proxyvagrant VM ovo gc_master
    config.vm.define "gc_client" do |proxyvagrant|
      proxyvagrant.vm.box = "bento/ubuntu-16.04"
      proxyvagrant.vm.network "private_network", type: "dhcp"
      proxyvagrant.vm.synced_folder "..", "/code"
  
      proxyvagrant.vm.provider "virtualbox" do |vb|
        # Customize the amount of memory on the VM:
        # vb.gui = true
        vb.memory = "2048"
        vb.cpus = 2
      end
    end
  end
  