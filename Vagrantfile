Vagrant.configure("2") do |config|
  config.vm.hostname = "gatling-work"
  config.vm.box = "precise64"
  config.omnibus.chef_version = :latest
  config.vm.network :private_network, ip: "33.33.33.10"
  config.vm.boot_timeout = 120
  config.berkshelf.enabled = true

  config.vm.provision :chef_solo do |chef|
    
    #chef.cookbooks_path = ["cookbooks"]

    chef.run_list = [
      "recipe[tnt-gatling::default]"
    ]
  end
end