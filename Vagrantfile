# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "sentry" do |sentry|
    # sentry.vm.box = "centos-6-4"
    # sentry.vm.box_url = "https://dl.dropboxusercontent.com/s/z85s74gv74m6flo/centos-6-4.box"
    # sentry.vm.box = "wheezy64"
    # sentry.vm.box_url = "https://dl.dropboxusercontent.com/s/j887m9989t2g8zj/wheezy64.box"
    #sentry.vm.box = "canonical/precise64"
    #sentry.vm.box_url = "http://files.vagrantup.com/precise64.box"
    sentry.vm.box = "canonical/trusty64"
    sentry.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    sentry.vm.provider "virtualbox" do |vb|
      vb.memory = 4096
      vb.cpus = 4
    end

    sentry.vm.network :private_network, ip: "192.168.33.10"

    sentry.vm.provision "ansible" do |ansible| 
      ansible.playbook = "sentry.yml"
      ansible.verbose = ''
    end 
  end

end
