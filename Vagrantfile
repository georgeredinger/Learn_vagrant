# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
 config.vm.box = "base"
# config.vm.boot_mode = :gui
 config.vm.forward_port 80,4567
 config.vm.provision :chef_solo do |chef|
   #chef.add_recipe "vagrant_main"
	 chef.add_recipe "apt"
	 chef.add_recipe "nginx"
	 chef.add_recipe "postgres"
	 chef.add_recipe "openssl"
 end

end

