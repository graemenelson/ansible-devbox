An Ansible playbook that setups a consistent ubuntu development box, on Vagrant or any of the cloud providers.

**NOTE:** only the software is installed, no application specific state is added to the box.

# Setup

### Vagrant

To use a local vagrant box, just run:

    vagrant up

Once the step is done, you can access the box with:

    ssh dev@172.17.8.100 -A

**NOTE:** the `-A` will allow access to your local ssh keys that have been added via `ssh-add`.

### Digital Ocean

Create a new `Ubuntu 14.04` droplet, using your machines ssh keys as the authentication method.

Update the `host` file with the droplet's `IP ADDRESS`, and then run the following command:

    ansible-playbook --user=root -i host playbook.yml

Once the ansible playook has completed, you can access the box:

    ssh dev@<IP ADDRESS> -A

**NOTE:** the `-A` will allow access to your local ssh keys that have been added via `ssh-add`.

# Next Steps
