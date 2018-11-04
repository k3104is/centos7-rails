Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.synced_folder "/works/vm/infra/workspace", "/home/vagrant/workspace"
#  config.vm.network "private_network", ip:"192.168.100.140"
  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--ostype", "RedHat_64"]
  end
  config.vm.provision "docker"
#  config.vm.provision "docker" do |d|
#    d.build_image "/vagrant", args: "-t hidekuro/my-bash"
#    d.run "hidekuro/my-bash", args: "-d -t -v /vagrant:/tmp/shared"
#  end
end
