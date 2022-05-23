# -*- mode: ruby -*-
# vi: set ft=ruby :
$hostsfile_update = <<-'SCRIPT'
echo -e '192.168.56.110 control.example.com control\n' >> /etc/hosts
SCRIPT

Vagrant.configure("2") do |config|

  config.vm.define "control", primary: true do |control|
    control.vm.box = "debian/stretch64"
    control.vm.box_version = "9.9.0"
    control.vm.hostname = "control.example.com"
    control.vm.network "forwarded_port", guest: 80, host: 8888
    control.vm.network "private_network", ip: "192.168.56.110"
    control.vm.provision "shell", inline: $hostsfile_update
    control.vm.provider "virtualbox" do |v|
    config.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--audio", "none"]
    end
 	v.memory = 2048
	v.cpus = 2
    end
  end

end
