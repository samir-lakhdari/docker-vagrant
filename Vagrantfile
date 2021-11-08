Vagrant.configure("2") do |config|
  config.vm.define "docker" do |master|
    docker.vm.box = "centos/7"
    docker.vm.hostname = "docker"
    docker.vm.network "private_network", ip: "192.168.56.10"
    docker.vm.provider "vmware_desktop" do |vm|
      vm.vmx["memsize"] = "2048"
      vm.vmx["numvcpus"] = "1"
      vm.gui = true
    end
    docker.vm.provision "shell", path: "install-docker.sh"
  end
end
