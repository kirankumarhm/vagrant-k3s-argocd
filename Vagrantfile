IMAGE_NAME = "bento/ubuntu-18.04"

Vagrant.configure("2") do |config|
    config.ssh.username = "vagrant"
    config.ssh.password = "vagrant"
    config.ssh.insert_key = true

    config.vm.provider "virtualbox" do |v|
        v.memory = 4096
        v.cpus = 2
        v.name = "K3S"
    end
      
    config.vm.define "K3S" do |k3s|
        k3s.vm.box = IMAGE_NAME
        k3s.vm.network "private_network", ip: "192.168.56.40"
        k3s.vm.hostname = "k3s-server"
    end
  
end