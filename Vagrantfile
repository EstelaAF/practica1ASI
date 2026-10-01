Vagrant.configure("2") do |config|

  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/jammy64"

    web.vm.hostname = "web"

    web.vm.network "private_network",
      ip: "192.168.56.10"

    web.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 1
    end

    web.vm.provision "shell",
      path: "provisioning.sh"
  end

  config.vm.define "cliente" do |cliente|
    cliente.vm.box = "ubuntu/jammy64"

    cliente.vm.hostname = "cliente"

    cliente.vm.network "private_network",
      ip: "192.168.56.11"
  end

end