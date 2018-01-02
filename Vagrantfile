# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.synced_folder ".", "/vagrant", type: "rsync",
    owner: "apache",
    group: "apache",
    mount_options: ["dmode=775, fmode=755"]

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vbguest.auto_update = false

  config.vm.provision "file", source: "~/.gitconfig", destination: "~/.gitconfig"
  config.vm.provision "file", source: "~/.vimrc", destination: "~/.vimrc"
  config.vm.provision "file", source: "httpd.conf", destination: "/etc/httpd/conf/httpd.conf"

  config.vm.provision "shell", path: "https://raw.githubusercontent.com/DMiller5383/vagrant/master/scripts/centos-lamp.sh"
end
