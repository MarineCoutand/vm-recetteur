Vagrant.configure("2") do |config|
  config.vm.box = "debian/stretch64"
  config.vm.hostname = "my-project-vm"
  config.vm.network "private_network", ip:"192.168.2.12"
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "2048"
    vb.customize ["modifyvm", :id, "--vram", "12"]
  end
  config.vm.provision "ansible" do |ansible|
  	ansible.verbose = "v"
  	ansible.playbook = "poste-recetteur-playbook.yaml"
  end
end



 
