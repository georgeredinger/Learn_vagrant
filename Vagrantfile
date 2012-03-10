# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
 config.vm.box = "base"
# config.vm.boot_mode = :gui
 config.vm.forward_port 80,4567
 config.vm.provision :chef_solo do |chef|
	 chef.cookbooks_path = "~/workspace/cookbooks"
   chef.add_recipe 'vagrant_main'
 end

end

