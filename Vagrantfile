# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.provision "docker" do |d|
    d.pull_images "dockerfile/nginx"
    d.run "dockerfile/nginx", args: "-p 80:80"
  end
  config.vm.network "forwarded_port", guest: 80, host:8080
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 4
  end
end