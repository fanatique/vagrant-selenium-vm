VAGRANTFILE_API_VERSION = "2"

dir = File.dirname(File.expand_path(__FILE__))

require 'yaml'

configValues = YAML.load_file("#{dir}/config.yml")
data = configValues['vagrantfile']

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_url = 'https://vagrantcloud.com/ubuntu/boxes/trusty64/versions/14.04/providers/virtualbox.box'

  config.vm.network :forwarded_port, guest:4444, host:4444
  config.vm.network :private_network, ip: "192.168.33.10"
  config.vm.provision "shell" do |s|
   s.path = "script.sh"
   s.args = data['host_entries']
  end
end
