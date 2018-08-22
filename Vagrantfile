# -*- mode: ruby -*-
# vi: set ft=ruby :

# SET YOUR HOSTNAME HERE
#################################
host_name = "joe-acfoundation"
#################################

Vagrant.configure("2") do |config|
  config.vm.hostname = "#{host_name}"
  config.vm.box = "laserred/neutrino"
  config.vm.network "public_network"
  config.vm.post_up_message = "*******************************************\n\nIf this is the first boot of this box,\nyou will need to reboot it \nbefore you can access it by hostname\n\n*******************************************\n\nLaser Red Neutrino is now running on: #{host_name}.local"
  config.vm.synced_folder "www", "/var/www",
	:owner => 'vagrant',
        :group => 'www-data',
        :mount_options => ['dmode=775', 'fmode=775']
  config.vm.provision "shell", inline: "sudo ee site create #{host_name}.local --php7 --wp"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

end
