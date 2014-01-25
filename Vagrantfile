Vagrant.configure("2") do |config|

  config.vm.define :centos6 do |centos6|
    centos6.vm.box      = 'opscode-centos-6.5'
    centos6.vm.box_url  = 'http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-6.5_chef-provisionerless.box'
    centos6.vm.hostname = "centos65"
  end

  config.vm.define :saucy do |saucy|
    saucy.vm.box      = 'saucy'
    saucy.vm.box_url  = 'http://cloud-images.ubuntu.com/vagrant/saucy/current/saucy-server-cloudimg-amd64-vagrant-disk1.box'
    saucy.vm.hostname = "ubuntu"
  end

  config.vm.network :private_network, ip: '10.0.1.2'
  config.vm.network "forwarded_port", guest: 80, host: 8000

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", 1024]
  end

end
