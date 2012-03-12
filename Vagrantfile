# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
 config.vm.customize ["modifyvm", :id, "--memory", 256]
 config.vm.box = "base"
 config.vm.share_folder("foobar","/home/vagrant/workspace/di","~/workspace/di")
 config.vm.forward_port 80,4567
 config.vm.forward_port 3000,3000

 config.vm.provision :chef_solo do |chef|
   chef.log_level = :debug

	 chef.cookbooks_path = "~/workspace/cookbooks"
   chef.add_recipe 'vagrant_main'
   chef.add_recipe 'chef-rbenv'
 end

end

