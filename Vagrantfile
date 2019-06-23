Vagrant.require_version ">= 1.7"

PROJECT_NAME = "win10"

# Workaround for macOS issue (https://github.com/ansible/ansible/issues/32499#issuecomment-401191857)
ENV["VAGRANT_OLD_ENV_OBJC_DISABLE_INITIALIZE_FORK_SAFETY"] = "YES"

Vagrant.configure("2") do |config|
    config.vm.provider "virtualbox" do |v|
        v.name = PROJECT_NAME
        v.memory = 2048
        v.cpus = 2
        v.gui = true
    end

    config.vm.box = "StefanScherer/windows_10"
    config.vm.network :private_network, ip: "192.168.22.11"

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "ansible/playbook.yml"
        ansible.inventory_path = "ansible/inventories/hosts.ini"
        ansible.limit = "all"
        ansible.compatibility_mode = "2.0"
        # ansible.verbose = "vvvv"
    end
end
