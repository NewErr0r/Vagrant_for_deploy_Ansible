Vagrant.configure("2") do |config|

 #--------------------------------APP-GW----------------------------------------- 
 
 config.vm.define "gw" do |gw|
  gw.vm.hostname = "APP-GW"
  gw.vm.box = "generic/centos8s"
  gw.vm.network "public_network", bridge: "br0", ip: "192.168.0.150"

  gw.vm.provider "virtualbox" do |vb|
    vb.name = "APP-GW"
    vb.cpus = 1
    vb.memory = "1024"
  end

  gw.vm.provision "shell", inline: <<-SHELL
  sudo echo "root:toor" | chpasswd
SHELL
end
#--------------------------------APP-VM01----------------------------------------- 

config.vm.define "vm01" do |vm01|
  vm01.vm.hostname = "APP-VM01"
  vm01.vm.box = "generic/centos8s"
  vm01.vm.network "public_network", bridge: "br0", ip: "192.168.0.151"

  vm01.vm.provider "virtualbox" do |vb|
    vb.name = "APP-VM01"
    vb.cpus = 1
    vb.memory = "1024"
  end

vm01.vm.provision "shell", inline: <<-SHELL
  sudo echo "root:toor" | chpasswd
SHELL
end
#--------------------------------APP-VM02----------------------------------------- 

config.vm.define "vm02" do |vm02|
  vm02.vm.hostname = "APP-VM02"
  vm02.vm.box = "generic/centos8s"
  vm02.vm.network "public_network", bridge: "br0", ip: "192.168.0.152"
  
  vm02.vm.provider "virtualbox" do |vb|
    vb.name = "APP-VM02"
    vb.cpus = 1
    vb.memory = "1024"
  end

  vm02.vm.provision "shell", inline: <<-SHELL
  sudo echo "root:toor" | chpasswd
SHELL
end
#-----------------------------------------------------------------------------------
end