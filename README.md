# Docker Vagrant Box

A simple vagrant box based on Ubuntu 18.04 with Docker and Docker Compose installed and partially configured.

## Why?

If you've tried running Docker on a Mac, you might have an idea. The filesystem is rather slow on the Docker version of MacOS -- so much so that even running Docker within a VM is faster. So, here you have it. This is just how I do it, but others might have a better way. Feel free to use this box if it benefits your workflow, or create a pull request if you have anything you think might benefit this box!

## How?

Clone this repo into a directory of your choosing and change into the newly-created directory.

Run the following command:

```bash
$ vagrant up
```

You can now SSH into your newly-provision Vagrant box and start using Docker from there.

```bash
$ vagrant ssh
```

## Configuration

By default the Vagrantfile will map the `code` directory within your home folder (`~/code`) to the vagrant user's home directory. If you would like to map other directories, feel free to change this line in the Vagrantfile to something else:

```
config.vm.synced_folder "~/code", "/home/vagrant/code"
```