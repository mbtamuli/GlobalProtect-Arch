# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "archlinux/archlinux"

  config.vm.synced_folder '.', '/vagrant'
  config.vm.provision "shell", inline: <<-SHELL
    sudo pacman -Syy base-devel
    mkdir -p globalprotect-build
    cp /vagrant/PKGBUILD globalprotect-build/
    cp /vagrant/GlobalProtect.install globalprotect-build/
  SHELL
end
