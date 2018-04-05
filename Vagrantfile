VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "bento/centos-7.4"

  config.vm.define :mk do | mk |
    mk.vm.hostname = "mysql"
    mk.vm.network :private_network, ip: "192.168.33.105"#, virtualbox__intnet: "intnet"
    mk.vm.provision :shell, :path => "./init.sh",:privileged   => true
  end

end
