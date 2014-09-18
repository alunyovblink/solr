Vagrant.configure("2") do |config|

  # Defines the Vagrant box name, download URL, IP and hostname
  config.vm.define :vagrant do |vagrant|
    vagrant.vm.box = "precise64"
    vagrant.vm.box_url = "http://files.vagrantup.com/precise64.box"

    vagrant.vm.network :private_network, ip: "192.168.66.6"
    vagrant.vm.network "forwarded_port", guest: 8983, host: 8983

    vagrant.vm.hostname = "vagrant.dcl"

    config.vm.provision :shell, path: "scripts/bootstrap.sh"
  end
end
