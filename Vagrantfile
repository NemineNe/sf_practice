# -*- mode: ruby -*-
# vi: set ft=ruby :
ENV['VAGRANT_SERVER_URL']="https://vagrant.elab.pro"

Vagrant.configure(«2») do |config|
 config.vm.box = «ubuntu/bionic64»

 config.vm.provision «shell», inline: <<-SHELL
  apt-get update
  apt-get -y upgrade
  apt-get install python3
  apt-get install python3-pip
  pip3 install psycopg2
  pip3 install django

 SHELL
 
 config.vm.provision "file", source: "~/test_file", destination: "test_file"
end
