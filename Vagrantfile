# frozen_string_literal: true

# Конфигурация Vagrant версии 2
Vagrant.configure("2") do |config|
  # Общие настройки для всех виртуальных машин
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus = 2
  end

  # Конфигурация для ALT Linux
  config.vm.define "alt" do |conf|
    conf.vm.box = "alt11"
    conf.vm.box_url = "file:///home/flick/ansible/alt.box"
  end

  # Конфигурация для Astra Linux
  config.vm.define "astra" do |conf|
    conf.vm.box = "astra"
    conf.vm.box_url = "file:///home/flick/ansible/astra.box"
  end

  config.vm.define "redos" do |conf|
    conf.vm.box = "redos"  # Образ RED OS
    conf.vm.box_url = "file:///home/flick/ansible/redos.box"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "main.yaml"
  end
end
