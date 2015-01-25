VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision "shell",
      inline: "apt-get -y update && apt-get -y upgrade && apt-get -y install nodejs-legacy nodejs npm && debconf-set-selections <<< 'mysql-server mysql-server/root_password password password' && debconf-set-selections <<< 'mysql-server mysql-server/root_password_again password password' && apt-get install -y mysql-server && apt-get -y install git && echo 'CREATE DATABASE `database`;' | mysql -uroot -ppassword && git clone 'https://github.com/QuinnEbert/ExpressJS_Sequelize_MySQL_Template.git' '/home/vagrant/myApp' && cd /home/vagrant/myApp && npm install"
  config.vm.network "public_network", bridge: 'en0: Ethernet'
   config.vm.provider "virtualbox" do |vb|
     vb.customize ["modifyvm", :id, "--memory", "800"]
   end
end
