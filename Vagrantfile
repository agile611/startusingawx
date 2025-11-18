Vagrant.configure(2) do |config|
  config.vm.define "awx" do |awx|
    awx.vm.box = "bento/ubuntu-24.04"
    awx.vm.network "private_network", ip: "192.168.11.50"
    awx.vm.hostname = "awx"
    awx.vm.network "forwarded_port", guest: 32000, host: 32000
    awx.vm.provider "virtualbox" do |vb|
      vb.memory = "4096"
      vb.cpus = "2"
    end
  end
end
