# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
 config.vm.box = "ubuntu/trusty64" 
 config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.define "control" do |control|
    config.vm.box = "ubuntu/xenial64"
    control.vm.network :public_network, bridge: "wlp2s0", ip: "192.168.0.110"
  end

  config.vm.define "db" do |db|
    db.vm.network :public_network, bridge: "wlp2s0", ip: "192.168.0.111"
  end

  config.vm.define "dbel" do |db|
    db.vm.network :public_network, bridge: "wlp2s0", ip: "192.168.0.112"
    db.vm.box = "opscode_centos-6.5-x86"
    db.vm.box = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-6.8_chef-provisionerless.box"
  end

  config.vm.define "www" do |www|
    www.vm.network :public_network, bridge: "wlp2s0", ip: "192.168.0.113"
  end

  config.vm.define "lb" do |lb|
    lb.vm.network :public_network, bridge: "wlp2s0", ip: "192.168.0.114"
  end

  config.vm.define "nginx" do |nginx|
    nginx.vm.network :public_network, bridge: "wlp2s0", ip: "192.168.0.115" 
  end
end
