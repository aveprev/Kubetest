Vagrant.configure("2") do |config|
  (1..3).each do |i|
    config.vm.define "node" + i.to_s, primary: (i == 1) do |node|
      node.vm.box = "centos/7"

      node.vm.provision "ansible" do |ansible|
        ansible.playbook = "install-docker-playbook.yml"
      end
    end
  end
end
