# HOWTO Configure Development Environment

## Requirements
* Vagrant: https://www.vagrantup.com/downloads.html
* Virtualbox: https://www.virtualbox.org/wiki/Downloads

## Istructions
1. Retrieve GIT Repository:
   * ```sudo apt install git```
   * ```cd /opt/ ; git clone https://github.com/malavolti/vagrant4ansible``` 
2. Move on the "```vagrant4ansible```" directory extracted.
   * ```cd /opt/vagrant4ansible```
3. Install the Guest Additions with "```vagrant plugin install vagrant-vbguest```"
4. Install the Vagrant plugin to resize hard disk (10GB): "```vagrant plugin install vagrant-disksize```"
5. Run "```vagrant up```" command to instance the Development Environment.
6. Change your own "```/etc/hosts```" (Linux) or "```C:\Windows\System32\drivers\etc\hosts```" (Windows) and add a name for you Development Environment:

    ```192.168.33.10  idp.example.org```
   
7. Now you are able to access to the Development Environment Server "```idp.example.org```" (192.168.33.10) with "```vagrant```" as username and your own SSH Key from Putty, MobaXTerm, Babun, ... 
   and it will possible to see your Apache2 sites directly from your preferred Browser Internet (Chrome, FireFox, Opera, ...)

## Useful Commands
1. To shutdown the Development Environment use "```vagrant halt```" within the "```cmd```" prompt (Windows)

2. To reload the Development Environment use "```vagrant reload```" within the "```cmd```" prompt (Windows)

3. To destroy the Development Environment use "```vagrant destroy```" within the "```cmd```" prompt (Windows)
