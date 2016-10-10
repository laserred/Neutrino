# Neutrino
An uncluttered Vagrant setup for building PHP websites. 

### Installation
1. Clone this repo into your project folder.
2. Edit the Vagrantfile to add a hostname.
3. `vagrant up`
4. On first boot, you will need to run `vagrant reload` in order for the hostname to be recognised on the network.
5. READ THE LINE ABOVE, EVERYONE FORGETS THIS. (You only need to do it once so Avahi can broadcast your hostname.)

### Info
This Vagrant box uses [EasyEngine](https://easyengine.io) so creating new sites is as simple as typing:

`sudo ee site create http://your-hostname.local`

See the [EasyEngine documentation](https://easyengine.io/docs/) for command line switches for adding PHP, MySQL, WordPress etc.

### Box info
Ubuntu 16.04.1

EasyEngine 3.7.4

Avahi Daemon for multicast DNS.
