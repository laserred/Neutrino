# -*- mode: ruby -*-
# vi: set ft=ruby :

# SET YOUR HOSTNAME ADDRESS HERE
# After reboot the box will be available at http://host_name.local
#

#################################

host_name = "test"

#################################


Vagrant.configure("2") do |config|
    config.vm.box = "laserred/neutrino"
    config.vm.hostname = "#{host_name}"
    config.vm.network "public_network"
    config.vm.post_up_message = "*******************************************\n\nIf this is the first boot of this box,\nyou will need to reboot it \nbefore you can access it by hostname\n\n*******************************************\n\nLaser Red Neutrino is now running on: #{host_name}.local"
    config.vm.provision :shell, inline: "hostnamectl set-hostname #{host_name}"
    config.vm.synced_folder "www/", "/var/www"
    config.ssh.username = "vagrant"  
    config.ssh.password = "vagrant"      
end
