# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64_vmware_fusion.box"

  config.vm.network :forwarded_port, guest: 80, host: 8001

  config.vm.provision :puppet do |puppet|
      puppet.manifests_path = "puppet/manifests"
      puppet.manifest_file  = "boilerplate.pp"
      puppet.module_path = "puppet/modules"
  end

end
