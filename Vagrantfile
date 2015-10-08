# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "sentry" do |sentry|
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end

    sentry.vm.box = "ubuntu/trusty64"
    sentry.vm.network :private_network, ip: "192.168.33.10"
    # sentry.vm.network "forwarded_port", guest: 80, host: 8895

    sentry.vm.provision "ansible" do |ansible|
      ansible.playbook = "site.yml"
      ansible.verbose = 'v'
    end
  end

end
