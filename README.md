# raspberry-hosting
Configure a Raspberry Pi to host services using Docker

## Using the local development box
Make sure you have [Vagrant](https://vagrantup.com) installed. Then run

    vagrant up
    
and wait for the Raspberry Pi machine to be 'up and running'.

## Running the Ansible Playbooks
Make sure you have [Ansible](https://www.ansible.com) installed. If needed you can change the hostname of your Raspberry
Pi in the file `production.ini` (the default value assumes the Pi is available using the default hostname `raspberrypi`).

To setup your Raspberry Pi run the `first_user.yml` playbook. This will change the default password of the `pi` user and
creates a new (SSH) user to connect with your Raspberry Pi server.

    ansible-playbook -k -K first_user.yml