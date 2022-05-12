# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "TimeS-Dev/centos7wpse"
  config.vm.box_version = "0.0.1"
  
  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", ip: "192.168.56.3", netmask: "255.255.255.0"

  # SSH settings
  config.ssh.password = "vagrant"
  config.ssh.insert_key = false
  config.ssh.keys_only = false

  # Fix a problem with Wordpress
  config.vm.provision :shell, path: "bootstrap.sh"
end
