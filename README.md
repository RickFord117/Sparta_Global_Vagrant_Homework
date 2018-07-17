This is a guide to installing and utilising a Vagrant machine.

Before beginning, you must ensure that your machine has Vagrant installed.

Once Vagrant is installed, start by opening your console and creating your file directory. You should also install nginx while on this screen if you don't already have it. Do this by using the following command: 'sudo apt-get nginx -y'
You will use this to create web servers for your code to run on.
Again, you should also install hostsupdater which you can use to add a domain name to your server. Do this with the following command: 'vagrant plugin install vagrant-hostsupdater'

Use the command 'vagrant init' to prepare and add a vagrant configuration file to your directory.

Use Atom or another source code editor to start adding your desired settings to your config file. A good start would be to remove all the comments so that the file is easier to read.

You can now choose which Virtual machine you would like to run by specifying it using config.vm.box = "vm name" inside the config loop.

Specify what the IP address of your nginx server using config.vm.network "private_network", ip: "IP address"
When your server is up and running, you can use this address to access it.

You can also set a Domain name for your address by using config.hostsupdater.aliases = ["doman name"].
When your server is up and running, using this domain name in the URL will point to your IP address.

Once your config file is set up, Use the command: 'vagrant up' to prepare your directory once more, then use: 'vagrant ssh' to enter the VM and start the server.
You can now test to see that your server is running by using the command ifconfig and comparing the IP addresses that are shown to you with the one specified inside the config file. You should also be able to hit the nginx splash page when you type in this IP into the URL. The same effect should occur when you type your domain name into the URL.
