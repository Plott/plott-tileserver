Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision "docker" do |d|
    d.pull_images "nginx"
    # d.pull_images "vagrant"
    d.run "nginx",
      cmd: "bash -l",
      args: "-v '/vagrant:/var/www'"
  end
  config.vm.network :forwarded_port, guest: 80, host: 4567
end
