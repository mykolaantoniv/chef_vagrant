Vagrant.configure(2) do |config|
  
  config.vm.define "node" do |node|
    node.vm.box = "ubuntu/trusty64"
    node.vm.network "private_network", ip:"192.168.0.3"
    node.vm.hostname = "node.example.com"
   end

  config.vm.define "workstation" do |workstation|
    workstation.vm.box = "ubuntu/trusty64"
    workstation.vm.network "private_network", ip: "192.168.0.252"
    workstation.vm.hostname = "workstation.example.com"
   end

  config.vm.define "chef" do |chef|
    chef.vm.box = "ubuntu/trusty64"
    chef.vm.network "private_network", ip: "192.168.0.253"
    chef.vm.hostname ="chef.example.com"
    chef.vm.provider "virtualbox" do |v|
   end

  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", inline: <<-SHELL
     sudo apt-get update
    SHELL
end
