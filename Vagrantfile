# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Base box for all nodes
  config.vm.box = "ubuntu/focal64"

  # Master Node Configuration
  config.vm.define "h_master" do |master|
    master.vm.hostname = "h-master"
    master.vm.network "private_network", ip: "198.100.68.10"
    master.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
    master.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y openjdk-11-jdk
      echo "Master node setup complete."
    SHELL
  end

  # Worker Node 1 Configuration
  config.vm.define "h_worker1" do |worker1|
    worker1.vm.hostname = "h-worker1"
    worker1.vm.network "private_network", ip: "198.100.68.20"
    worker1.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
    worker1.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y openjdk-11-jdk
      echo "Worker node 1 setup complete."
    SHELL
  end

  # Worker Node 2 Configuration
  config.vm.define "h_worker2" do |worker2|
    worker2.vm.hostname = "h-worker2"
    worker2.vm.network "private_network", ip: "198.100.68.30"
    worker2.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
    worker2.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y openjdk-11-jdk
      echo "Worker node 2 setup complete."
    SHELL
  end
end
