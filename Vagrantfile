# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vbguest.auto_update = false

  config.vm.provision "file", source: "~/.gitconfig", destination: "~/.gitconfig"

  config.vm.provision "shell", path: "https://raw.githubusercontent.com/DMiller5383/vagrant/master/scripts/centos-lamp.sh"
end
