Vagrant.configure('2') do |config|
	config.vm.box = 'debian/jessie64'
	config.vm.hostname = 'debian'

	config.vm.network :forwarded_port, guest: 3000, host: 3000
	config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true
	config.vm.synced_folder 'projects/', '/home/vagrant/projects/'

	config.vm.provider "virtualbox" do |v|
		v.memory = 1024
		v.cpus = 2
	end
end
