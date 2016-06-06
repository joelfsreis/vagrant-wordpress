#HOSTNAME = File.basename(File.dirname(__FILE__), ".git")

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
#VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(2) do |config|

#  config.vm.hostname = HOSTNAME

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1048
    v.cpus = 1
  end
  config.vm.network :private_network, ip: "10.11.12.13"

  config.vm.synced_folder ".", "/vagrant", type: "nfs"

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
