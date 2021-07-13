# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  #vagrant plugin install vagrant-env
  config.env.enable
  config.vm.provider "virtualbox" do |v|
    v.memory = 6048
    v.cpus = 4
  end
  config.vm.define "server" do |machine|
    machine.vm.network "private_network", ip: "10.2.2.25"
    machine.vm.box = "ubuntu/bionic64"
    machine.vm.provision :ansible do |ansible|
      ansible.playbook = ENV["PLAYBOOK_NAME"]
      ansible.verbose = 'vv'
    end
  end
end