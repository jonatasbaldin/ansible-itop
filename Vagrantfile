# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "vvv"
    ansible.sudo = "true"
    ansible.playbook = "site.yml"
  end

  config.vm.define "itop" do |itop|
    itop.vm.network  "public_network"
    itop.vm.hostname = "itop"
  end

end
