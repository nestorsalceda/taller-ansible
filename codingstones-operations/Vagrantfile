# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "debian/jessie64-additions"

  config.vm.define "wip" do |sut|
    config.vm.network "private_network", ip: "10.0.0.2"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "wip.yml"
    ansible.sudo = true
  end
end
