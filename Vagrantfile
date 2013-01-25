Vagrant::Config.run do |config|

  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.forward_port 80, 8080
  config.vm.forward_port 3306, 3306

  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "chef/cookbooks"
    chef.add_recipe "chef-lamp"

    chef.json = {
      :mysql => {
        :server_root_password => "rootpwd",
        :server_repl_password => "rootpwd",
        :server_debian_password => "rootpwd",
        :allow_remote_root => true
      }
    }
  end
end