Vagrant.configure(2) do |config|
  config.vm.define "awx" do |awx|
    awx.vm.box = "bento/ubuntu-24.04"
    awx.vm.network "private_network", ip: "192.168.10.50"
    awx.vm.hostname = "awx"
    #awx.vm.provision :shell, :path => "docker.sh"
    #awx.vm.provision :shell, :path => "ansible.sh"
    awx.vm.network "forwarded_port", guest: 80, host: 80
    awx.vm.network "forwarded_port", guest: 443, host: 443
    #awx.vm.network "forwarded_port", guest: 3000, host: 3000
    awx.vm.network "forwarded_port", guest: 8000, host: 8000
    awx.vm.network "forwarded_port", guest: 32000, host: 32000
    awx.vm.provider "virtualbox" do |vb|
      vb.memory = "4096"
      vb.cpus = "2"
    end
  end
end
