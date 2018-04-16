# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "debian-9.4-amd64"

  config.ssh.insert_key = false

  # Set libvirt to local only
  config.vm.provider :libvirt do |libvirt|
    libvirt.connect_via_ssh = false
  end

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file  = "default.pp"
    #puppet.options = "--verbose --debug"
  end
end
