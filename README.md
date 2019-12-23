# HOWTO Configure Development Environment

## Requirements to install before the next instructions
* Vagrant: https://www.vagrantup.com/downloads.html     (Tested with v2.0.3, v2.0.4 & v2.1.2 & 2.2.6)
* Virtualbox: https://www.virtualbox.org/wiki/Downloads (Tested with v5.2.10 & v5.2.18 & 6.0.14)

## Istructions for Linux
1. Retrieve GIT Repository:
   * `sudo su -`
   * `apt install git`
   * `cd /opt/ ; git clone https://github.com/malavolti/vagrant4ansible` 
   or
   * Download from `https://github.com/malavolti/vagrant4ansible/archive/master.zip` into `/opt` directory
2. Move on the "`vagrant4ansible`" directory extracted.
   * `cd /opt/vagrant4ansible`
3. Install the Guest Additions with "`vagrant plugin install vagrant-vbguest`"
4. Run "`vagrant up`" command to instance the Development Environment.
5. Change your own "`/etc/hosts`" (Linux) and add this line for the Development Environment:
   ```bash
   192.168.33.10 vm.example.org vm
   ```
6. Now you are able to access to the Development Environment Server "`vm.example.org`" with "`vagrant ssh`" and it will possible to see your Apache2 sites directly from your preferred Browser Internet (Chrome, FireFox, Opera, ...)

7. If you need to run Ansible only for the machine you have downloaded, add these lines on the Vagrant file:
   ```bash
   mkdir /etc/ansible
   echo "localhost	ansible_connection=local" > /etc/ansible/hosts
   ```

## Istructions for MacOSX
1. Retrieve GIT Repository:
   * `cd Desktop ; git clone https://github.com/malavolti/vagrant4ansible` 
   or
   * Download from `https://github.com/malavolti/vagrant4ansible/archive/master.zip`
2. Move on the "`vagrant4ansible`" directory extracted.
3. Install the Guest Additions with "`vagrant plugin install vagrant-vbguest`"
4. Run "`vagrant up`" command to instance the Development Environment.
5. Change your own "`sudo vi /private/etc/hosts`" and add this line for the Development Environment:
   ```bash
   192.168.33.10 vm.example.org vm
   ```
6. Now you are able to access to the Development Environment Server "`vm.example.org`" with "`vagrant ssh`" and it will possible to see your Apache2 sites directly from your preferred Browser Internet (Chrome, FireFox, Opera, ...)

7. If you need to run Ansible only for the machine you have downloaded, add these lines on the Vagrant file:
   ```bash
   mkdir /etc/ansible
   echo "localhost	ansible_connection=local" > /etc/ansible/hosts
   ```
   
## Istructions for Windows
1. Download the Repository from: https://github.com/malavolti/vagrant4ansible/archive/master.zip
2. Extract the ZIP file on your computer as "`vagrant4ansible`".
3. Run "`cmd`" command (Windows) as Administrator and move on the "`vagrant4ansible`" directory extracted.
4. Install the Guest Additions with "`vagrant plugin install vagrant-vbguest`"
5. Run "`vagrant up`" command to instance the Development Environment.
6. Change your hosts file on "`C:\Windows\System32\drivers\etc\hosts`" (Windows) and add this line the Development Environment:
   ```bash
   192.168.33.10 vm.example.org vm
   ```
7. Now you are able to access to the Development Environment Server "`vm.example.org`" and it will possible to see your Apache2 sites directly from your preferred Browser Internet (Chrome, FireFox, Opera, ...)

8. If you need to run Ansible only for the machine you have downloaded, add these lines on the Vagrant file:
   ```bash
   mkdir /etc/ansible
   echo "localhost	ansible_connection=local" > /etc/ansible/hosts
   ```

## Useful Commands (to use inside 'vagrant4ansible' dir)
1. To shutdown the Development Environment use "`vagrant halt`" within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

2. To reload the Development Environment use "`vagrant reload`" within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

3. To destroy the Development Environment use "`vagrant destroy`" within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

4. To use the Development Environment use "`vagrant ssh`" (to connect into the VM) and "`sudo su`" (to obtain ROOT access) within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

5. To manage Snapshot in Vagrant:
   1. Move in the vagrant VM directory and create a snapshot called "NAME_SNAPSHOT":

      `vagrant snapshot save NAME_SNAPSHOT`

   2. Recover your "`NAME_SNAPSHOT`":

      `vagrant snapshot restore NAME_SNAPSHOT`

   3. (OPTIONAL) List Snapshot:

      `vagrant snapshot list`

   4. (OPTIONAL) Remove Snapshot:

      `vagrant snapshot delete NAME_SNAPSHOT`

6. To update your Vagrant Box use "`vagrant box update`".
