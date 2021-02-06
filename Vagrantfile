Vagrant.configure('2') do |config|
    config.vm.define 'centos01' do |hyperv| 
      hyperv.vm.hostname = 'centos01'
      config.vm.box = "bento/centos-8" 
      hyperv.vm.network :private_network, ip: '192.168.99.201'
      config.vm.provider 'hyperv' do |h| 
        h.memory = 4096
        h.cpus = 4
      end
      config.vm.provision "shell", path: "bootstrap.sh"
    end
  end
  