# -*- mode: ruby -*-
# vi: set ft=ruby :

=begin provisioning
$ dst update
$ dst setup base # ipynb passwd required => no automatic provisioning
$ sudo apt-get update # required (maybe?) to install Chromium
$ dst add jhudss
=end

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "data-science-toolbox/dst"
  config.vm.box_version = ">= 0.2.1"

  config.vm.network "forwarded_port", guest: 8888, host: 8888

  config.vm.synced_folder "science_data", "/science_data"

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end
end
