# Vagrant Selenium VM

A very basic Vagrant machine running headless Chrome and Firefox under Ubuntu Linux 14.04.

## Requirements

- [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](http://vagrantup.com)

## Setup

    git clone https://github.com/fanatique/vagrant-selenium-vm.git
    cd vagrant-selenium-vm
    vagrant up

The provisioning should end with:

   ...
   ==> default: Done downloading and installing basic packages
   ==> default: Starting Xvfb ...
   ==> default: Starting Google Chrome ...
   ==> default: Starting Selenium ...

Afterwards the machine runs on a private network and can be found under `192.168.33.10`. 
Selenium is automatically started and runs on port `4444`, which is forwarded to the host.

Firefox and Chrome are installed and tested to be available for selenium tests.


