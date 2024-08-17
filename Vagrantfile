Vagrant.configure("2") do |config|
  config.ssh.insert_key = false

  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/jammy64"

    # Public network configuration
    master.vm.network "public_network"

    # Ansible provisioner
    master.vm.provision "ansible" do |ansible|
      ansible.playbook = "api-proxy.yml"
      ansible.inventory_path = "inventory/hosts"
    end
  end

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
    vb.cpus = "1"
  end
end
