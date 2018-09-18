Vagrant.configure("2") do |config|
config.vm.provision "shell", inline: "apt-get install -y telnet wget curl vim && echo 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDF98fBcTXQD8oyP85wsaUeA3BWGCsqSY5yRCt4qYb+k2NOpFs+AD8teLAYUOB7PCkz0lagqQKs2gNHOXfUIuK1YlOzFWZ7IG/ZU03tWXEo5HAZfkQ4y8NOfT2K0vlwHPis2v/T6HOEDao7bpslfCHJvHJWtRguaYgYIM0iwG3FUUA3d4VuVRA5t7J+COXwjfBj425imuDAkIAF8vEigL5eqedZ4iaAVX706+GwRFyj812JyR0WtzGuipq8bne05/f26srRUQppQJrwCr+7dzyHCG5gswHpD/1Dldk5EB2UaqoPJTFH73+aioMYuyF53rKBRGD1u34IpOdVGT2F2syp' >>~/.ssh/authorized_keys"
  config.vm.define "mongo" do |mongo|
    mongo.vm.box = "ubuntu/xenial64"
    mongo.vm.hostname = 'mongo'
    mongo.vm.network :private_network, bridge: "en0: Wi-Fi (AirPort)", ip: "192.168.10.40"
    mongo.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--cpus", 1]
      v.customize ["modifyvm", :id, "--name", "mongo"]
  end
end


  config.vm.define "mongo1" do |mongo1|
    mongo1.vm.box = "ubuntu/xenial64"
    mongo1.vm.hostname = 'mongo1'
    mongo1.vm.network :private_network, bridge: "en0: Wi-Fi (AirPort)", ip: "192.168.10.41"
    mongo1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--cpus", 1]
      v.customize ["modifyvm", :id, "--name", "mongo1"]
    end
  end

  config.vm.define "mongo2" do |mongo2|
    mongo2.vm.box = "ubuntu/xenial64"
    mongo2.vm.hostname = 'mongo2'
    mongo2.vm.network :private_network, bridge: "en0: Wi-Fi (AirPort)", ip: "192.168.10.42"
    mongo2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--cpus", 1]
      v.customize ["modifyvm", :id, "--name", "mongo2"]
    end

end
end