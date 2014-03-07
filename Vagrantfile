# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "nan-do"
  config.vm.box_url = "https://s3.amazonaws.com/nandorocker-vagrant-boxes/nan-do.box"
  config.vm.network :forwarded_port, guest: 80, host: 8090
  #config.vm.provision "shell", path: "config/basic_lamp.sh"

  # Small hack to allow chmod within the shared folder
  config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777,fmode=666"]
end