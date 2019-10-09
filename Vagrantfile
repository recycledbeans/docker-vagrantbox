Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.provision "shell", path: "scripts.sh"
  config.vm.synced_folder "~/code", "/home/vagrant/code"
end
