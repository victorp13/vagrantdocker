#VagrantDocker
First successful attempt at creating a Docker box with nginx on Vagrant.

####Setup Vagrant
To run, type "vagrant up"

Then ssh into the box via "vagrant ssh"

####Setup Docker
To install and run nginx:

* docker pull dockerfile/nginx
* docker run -d -p 80:80 dockerfile/nginx

####Success!
After this the nginx page can be opened on the Host via http://127.0.0.1:8080