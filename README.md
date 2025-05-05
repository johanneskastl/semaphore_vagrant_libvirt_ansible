# semaphore_vagrant_libvirt_ansible

This Vagrant-libvirt setup creates a VM and installs [Semaphore
UI](https://semaphoreui.com/), the modern UI for Ansible, Terraform, OpenTofu,
or Pulumi on the VM.

Default OS is openSUSE Leap 15.6. Although that can be changed in the
Vagrantfile, please beware that this will break the Ansible provisioning.

## Vagrant

1. You need vagrant obviously. And ansible. And git...
1. Fetch the box, per default this is `opensuse/Leap-15.6.x86_64`, using
   `vagrant box add opensuse/Leap-15.6.x86_64`.
1. Make sure the git submodules are fully working by issuing `git submodule init
   && git submodule update`
1. Run `vagrant up`
1. Open the URL that Ansible printed out at the end of the provisioning step. It
   should look something like `http://192.0.2.13:3000`.
   Log in using the credentials that Ansible also printed out: username `admin`
   and the password `totallysecurepassword`.
1. Party!

## Cleaning up

The VMs can be torn down after playing around using `vagrant destroy`.

## License

BSD-3-Clause

## Author Information

I am Johannes Kastl, reachable via git@johannes-kastl.de
