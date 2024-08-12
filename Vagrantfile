Vagrant.configure("2") do |config|
    config.ssh.insert_key = false
    config.vm.define "master" do |master|
      master.vm.box = "ubuntu/jammy64"
    end
    config.vm.network "public_network"
    bridge: "en0"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = "1"
    end
  end