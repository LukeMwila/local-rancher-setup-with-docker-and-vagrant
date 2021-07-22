Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-20.04"
    config.vm.define "rancher" do |rancher_dkr|
      rancher_dkr.vm.provision "shell", path: "script.sh"
      rancher_dkr.vm.network "private_network", ip: "172.16.128.4" 
      rancher_dkr.vm.hostname = "rancher"
      rancher_dkr.vm.provider "virtualbox" do |v|
        v.customize ["modifyvm", :id, "--audio", "none"]
        v.memory = 4024
        v.cpus = 2
      end
    end
end
  