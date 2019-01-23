# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|

  # normal setup
  config.vm.box = 'bento/ubuntu-16.04'
  config.vm.hostname = 'data-sci'
  config.vm.network 'private_network', type: :dhcp

  # enable ssh forwarding
  config.ssh.forward_agent = true

  config.vm.provider "virtualbox" do |v|
    v.memory = 8192
    v.cpus = 3
  end

  # forward ports for Zeppelin notebook (8080), Jupyter notebook (8888),
  # Jupyter slides (8000), Bokeh server (5006), and TensorFlow TensorBoard (6006)
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 8888, host: 8888
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.network "forwarded_port", guest: 5006, host: 5006
  config.vm.network "forwarded_port", guest: 6006, host: 6006

  # share the notebooks folder
  config.vm.synced_folder "notebooks/", "/home/vagrant/notebooks"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end
