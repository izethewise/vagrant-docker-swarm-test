# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

pkg_cmd = "wget -q -O - https://get.docker.io/gpg | apt-key add -;" \
        "echo deb http://get.docker.io/ubuntu docker main > /etc/apt/sources.list.d/docker.list;" \
        "apt-get update -qq; apt-get install -q -y --force-yes lxc-docker; "
        # Add vagrant user to the docker group
        pkg_cmd << "usermod -a -G docker vagrant; "

Vagrant.configure("2") do |config|

    config.vm.define "mgr1" do |mgr1|
        mgr1.vm.box = "phusion/ubuntu-14.04-amd64"
        mgr1.vm.hostname = 'mgr1'
        mgr1.vm.box_url = "phusion/ubuntu-14.04-amd64"

        mgr1.vm.network "private_network", ip: "172.31.12.161"
        
        mgr1.vm.provider :virtualbox do |v|
            v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
            v.customize ["modifyvm", :id, "--memory", 512]
            v.customize ["modifyvm", :id, "--name", "mgr1"]
        end
        
        config.vm.provision :shell, :inline => pkg_cmd
    end
    
        
    config.vm.define "mgr2" do |mgr2|
        mgr2.vm.box = "phusion/ubuntu-14.04-amd64"
        mgr2.vm.hostname = 'mgr2'
        mgr2.vm.box_url = "phusion/ubuntu-14.04-amd64"

        mgr2.vm.network "private_network", ip: "172.31.12.162"
        
        mgr2.vm.provider :virtualbox do |v|
            v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
            v.customize ["modifyvm", :id, "--memory", 512]
            v.customize ["modifyvm", :id, "--name", "mgr2"]
        end
        
        config.vm.provision :shell, :inline => pkg_cmd
    end
    
     
    config.vm.define "mgr3" do |mgr3|
        mgr3.vm.box = "phusion/ubuntu-14.04-amd64"
        mgr3.vm.hostname = 'mgr3'
        mgr3.vm.box_url = "phusion/ubuntu-14.04-amd64"

        mgr3.vm.network "private_network", ip: "172.31.12.163"
        
        mgr3.vm.provider :virtualbox do |v|
            v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
            v.customize ["modifyvm", :id, "--memory", 512]
            v.customize ["modifyvm", :id, "--name", "mgr3"]
        end
        
        config.vm.provision :shell, :inline => pkg_cmd
    end
    
    config.vm.define "wrk1" do |wrk1|
        wrk1.vm.box = "phusion/ubuntu-14.04-amd64"
        wrk1.vm.hostname = 'wrk1'
        wrk1.vm.box_url = "phusion/ubuntu-14.04-amd64"

        wrk1.vm.network "private_network", ip: "172.31.12.164"
        
        wrk1.vm.provider :virtualbox do |v|
            v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
            v.customize ["modifyvm", :id, "--memory", 512]
            v.customize ["modifyvm", :id, "--name", "wrk1"]
        end
        
        config.vm.provision :shell, :inline => pkg_cmd
    end
    
    config.vm.define "wrk2" do |wrk2|
        wrk2.vm.box = "phusion/ubuntu-14.04-amd64"
        wrk2.vm.hostname = 'wrk2'
        wrk2.vm.box_url = "phusion/ubuntu-14.04-amd64"

        wrk2.vm.network "private_network", ip: "172.31.12.165"
        
        wrk2.vm.provider :virtualbox do |v|
            v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
            v.customize ["modifyvm", :id, "--memory", 512]
            v.customize ["modifyvm", :id, "--name", "wrk2"]
        end
        
        config.vm.provision :shell, :inline => pkg_cmd
    end
    
    config.vm.define "wrk3" do |wrk3|
        wrk3.vm.box = "phusion/ubuntu-14.04-amd64"
        wrk3.vm.hostname = 'wrk3'
        wrk3.vm.box_url = "phusion/ubuntu-14.04-amd64"

        wrk3.vm.network "private_network", ip: "172.31.12.166"
        
        wrk3.vm.provider :virtualbox do |v|
            v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
            v.customize ["modifyvm", :id, "--memory", 512]
            v.customize ["modifyvm", :id, "--name", "wrk3"]
        end
        
        config.vm.provision :shell, :inline => pkg_cmd
    end
    
end
