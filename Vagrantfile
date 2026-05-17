Vagrant.configure("2") do |config|

  # =========================
  # Domain Controller
  # =========================
  config.vm.define "dc1" do |dc|
    dc.vm.box = "debian/bookworm64"
    dc.vm.hostname = "dc1.internal.local"

    dc.vm.network "private_network", ip: "192.168.56.20"

    dc.vm.provider "virtualbox" do |vb|
      vb.name = "dc1-samba4"
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  # =========================
  # Linux Client 1
  # =========================
  config.vm.define "client1" do |client|
    client.vm.box = "debian/bookworm64"
    client.vm.hostname = "client1.internal.local"

    client.vm.network "private_network", ip: "192.168.56.21"

    client.vm.provider "virtualbox" do |vb|
      vb.name = "client1-linux"
      vb.memory = 1024
      vb.cpus = 1
    end
  end

  # =========================
  # Linux Client 2
  # =========================
  config.vm.define "client2" do |client|
    client.vm.box = "debian/bookworm64"
    client.vm.hostname = "client2.internal.local"

    client.vm.network "private_network", ip: "192.168.56.22"

    client.vm.provider "virtualbox" do |vb|
      vb.name = "client2-linux"
      vb.memory = 1024
      vb.cpus = 1
    end
  end

end
