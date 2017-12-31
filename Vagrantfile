# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "chef/centos-6.5"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vbguest.auto_update = false

  config.vm.provision "file", source: "~/vagrant/file/git-config", destination: "~/.gitconfig"
end
