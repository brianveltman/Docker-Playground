# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure("2") do |config|
  config.vm.box = "brianveltman/docker-ce-stable"
  config.vm.box_version = "1.0.0"
  config.vm.box_check_update = false

  N = 2 # Number of Docker hosts to work with
  M = 3 # Number of Docker manager nodes to work with

  (1..N).each do |node_id|
    config.vm.define "docker_node#{node_id}" do |node|
      node.vm.hostname = "node-#{node_id}"
      node.vm.network "private_network", ip: "192.168.77.#{20+node_id}"
      end
    end

  (1..M).each do |manager_id|
    config.vm.define "docker_manager#{manager_id}" do |manager|
      manager.vm.hostname = "manager-#{manager_id}"
      manager.vm.network "private_network", ip: "192.168.77.#{21+manager_id}"
    end
  end  
end