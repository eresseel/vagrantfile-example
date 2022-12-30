# vagrant-example
This description applies to 19-creating-multiple-machines-with-disk-on-vm-folder vagrantfile.

## Table of variable

| variable        | must be used | example                                                                                             |
| --------------- | ------------ | --------------------------------------------------------------------------------------------------- |
| :box            | yes          |:box => "generic/ubuntu2004"                                                                         |
| :hostname       | yes          |:hostname => "test19-server"                                                                         |
| :ip             | yes          |:ip => "192.168.56.10"                                                                               |
| :ssh            | no           |:ssh => [ { :ssh_key_path => "files", :ssh_key_name => "id_rsa", :key_type => "rsa", :bit => 4096} ] |
| :port           | no           | :port => [ { :guest => "80", :host => "8888" } ]                                                    |
| :disk           | no           | :disks => [ { :disk_size => 10, :disk_type => "Standard"} ]                                         |
| :resource_limit | no           | :resource_limit => [ {:cpu => 1, :memory => 512} ]                                                  |
| :sync           | no           | :sync => [ { :src => ".", :dst => "/home/vagrant/vagrant" } ]                                       |
| :file           | no           | :files => [ { :src => "files/id_rsa", :dst => "/home/vagrant/.ssh/id_rsa" } ]                       |
| :sript          | no           | :script => "install.sh"                                                                             |
| :shell          | no           | :shell => provision_ansible                                                                         |
| :ansible        | no           | :ansible => [ { :limit => "client"} ]                                                               |
