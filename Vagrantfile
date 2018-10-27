# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

# Ensure yaml module loaded
require 'yaml'

settings = YAML.load_file('vagrant.yml')

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Define the base box and operating system for our server
  config.vm.box = settings['base_image']

  # Use the same key for each machine
  config.ssh.insert_key = false

  # Create a private network, which allows host-only access to the machine
  config.vm.network :private_network, ip: settings['ip_address']

  # Set hostname
  config.vm.hostname = settings['vm_name'] + "-" + settings['suffix']

  # Set the name of the VM.
  config.vm.define :"#{settings['vm_name']}" do |x|
  end

  # run Ansible from the Vagrant VM
  config.vm.provision "ansible_local" do |ansible|
    ansible.install = true
    ansible.playbook = "provisioning/playbook.yml"
  end

end
