Vagrant.configure("2") do |config|
  config.vm.box = "gvfoster/raspbian"

  #
  # Run Ansible from the Vagrant Host
  #
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
  end
end
