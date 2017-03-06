Vagrant.configure(2) do |config|

  config.vm.box = "hashicorp/precise64"

  config.vm.network "private_network", ip: "172.16.200.200"

  config.vm.provider "virtualbox" do |v|
    v.name = "tor"
    v.customize ["modifyvm", :id, "--memory", "512"]
    v.customize ["modifyvm", :id, "--usb", "off"]
    v.customize ["modifyvm", :id, "--usbehci", "off"]
  end

  config.vm.hostname = "tor"
  config.vm.provision "shell", path: "./scripts/bootstrap.sh"

end
