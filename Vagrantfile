# -*- mode: ruby -*-
# vi: set ft=ruby :

# Default box is xp-ie8
unless ENV['VAGRANT_BOX'] = ""
  BOX = "#{ENV['VAGRANT_BOX']}"
else
  BOX = "xp-ie8"
end

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.hostname = "#{BOX}"
  config.vm.box = "#{BOX}"
  config.vm.box_url = "http://aka.ms/vagrant-#{BOX}"
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.ssh.forward_agent = true
  # config.vm.synced_folder "../data", "/vagrant_data"
  config.vm.communicator = "winrm"
  config.vm.provider "virtualbox" do |vb|
  #   # Don't boot with headless mode
    vb.gui = true
  #   vb.customize ["modifyvm", :id, "--memory", "1024"]
  end
end
