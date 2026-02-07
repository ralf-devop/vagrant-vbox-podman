Vagrant.configure("2") do |config|

  config.vm.box = "bento/debian-13"
  config.vm.box_version = "202510.26.0"

  config.vm.network "forwarded_port", guest: 8088, host: 8088
  config.vm.network "forwarded_port", guest: 5432, host: 5432
  config.vm.network "forwarded_port", guest: 3306, host: 3306
  config.vm.network "forwarded_port", guest: 1521, host: 1521

  #config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "./ansible/playbook.yml"
  end

end
