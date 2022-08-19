Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  
  config.vm.synced_folder ".", "/vagrant"
  config.vm.provision "ansible_local" do |ansible|
    ansible.galaxy_role_file = "requirements.yml"
	ansible.galaxy_command = 'ansible-galaxy install --role-file=%{role_file} --ignore-errors'
    ansible.playbook = "playbook.yml"
  end
end
