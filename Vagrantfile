Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 3306, host: 33306
  config.vm.network "private_network", ip: "10.0.33.11"


  config.vm.synced_folder "application/", "/var/www/html/app", create: true

   config.vm.provider "virtualbox" do |vb|
     vb.gui = false
     vb.memory = "1024"
   end

   config.vm.provision "ansible" do |ansible|
           ansible.playbook = "playbook.yml"
           ansible.inventory_path = "hosts"
           ansible.limit = "all"
           end
	end
