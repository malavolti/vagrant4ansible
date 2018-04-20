# HOWTO Configure Development Environment

## Requirements to install before the next instructions
* Vagrant: https://www.vagrantup.com/downloads.html     (Tested with 2.0.3)
* Virtualbox: https://www.virtualbox.org/wiki/Downloads (Tested with 5.2.10)

## Istructions for Linux
1. Retrieve GIT Repository:
   * ```sudo apt install git```
   * ```cd /opt/ ; git clone https://github.com/malavolti/vagrant4ansible``` 
   or
   * Download from ```https://github.com/malavolti/vagrant4ansible/archive/master.zip```
2. Move on the "```vagrant4ansible```" directory extracted.
   * ```cd /opt/vagrant4ansible```
3. Install the Guest Additions with "```vagrant plugin install vagrant-vbguest```"
4. Install the Vagrant plugin to resize hard disk (10GB): "```vagrant plugin install vagrant-disksize```"
5. Run "```vagrant up```" command to instance the Development Environment.
6. Change your own "```/etc/hosts```" (Linux) and add these 2 lines for the Development Environment:
   ```bash
   192.168.33.10  idp.example.org
   192.168.44.10  sp.example.org
   ```
7. Now you are able to access to the Development Environment Server "```idp.example.org```" (192.168.33.10) or "```sp.example.org```" (192.168.44.10) with "```vagrant ssh```" and it will possible to see your Apache2 sites directly from your preferred Browser Internet (Chrome, FireFox, Opera, ...)

## Istructions for MacOSX
1. Retrieve GIT Repository:
   * ```cd Desktop ; git clone https://github.com/malavolti/vagrant4ansible``` 
   or
   * Download from ```https://github.com/malavolti/vagrant4ansible/archive/master.zip```
2. Move on the "```vagrant4ansible```" directory extracted.
   * ```cd /opt/vagrant4ansible```
3. Install the Guest Additions with "```vagrant plugin install vagrant-vbguest```"
4. Install the Vagrant plugin to resize hard disk (10GB): "```vagrant plugin install vagrant-disksize```"
5. Run "```vagrant up```" command to instance the Development Environment.
6. Change your own "```sudo vi /private/etc/hosts```" and add these 2 lines for the Development Environment:
   ```bash
   192.168.33.10  idp.example.org
   192.168.44.10  sp.example.org
   ```
7. Now you are able to access to the Development Environment Server "```idp.example.org```" (192.168.33.10) or "```sp.example.org```" (192.168.44.10) with "```vagrant ssh```" and it will possible to see your Apache2 sites directly from your preferred Browser Internet (Chrome, FireFox, Opera, ...)
   
## Istructions for Windows
1. Download the Repository from: https://github.com/malavolti/vagrant4ansible/archive/master.zip
2. Extract the ZIP file on your computer as "```vagrant4ansible```".
3. Run "```cmd```" command (Windows) as Administrator and move on the "```vagrant4ansible```" directory extracted.
4. Install the Guest Additions with "```vagrant plugin install vagrant-vbguest```"
5. Install the Vagrant plugin to resize hard disk (10GB): "```vagrant plugin install vagrant-disksize```"
6. Run "```vagrant up```" command to instance the Development Environment.
7. Change your hosts file on "```C:\Windows\System32\drivers\etc\hosts```" (Windows) and add these 2 lines the Development Environment:
   ```bash
   192.168.33.10  idp.example.org
   192.168.44.10  sp.example.org
   ```
8. Now you are able to access to the Development Environment Server "```idp.example.org```" (192.168.33.10) or "```sp.example.org```" (192.168.44.10) and it will possible to see your Apache2 sites directly from your preferred Browser Internet (Chrome, FireFox, Opera, ...)

## Useful Commands (to use inside 'vagrant4ansible' dir)
1. To shutdown the Development Environment use "```vagrant halt```" within the "```cmd```" prompt (Windows) or terminal (Linux/OSX)

2. To reload the Development Environment use "```vagrant reload```" within the "```cmd```" prompt (Windows) or terminal (Linux/OSX)

3. To destroy the Development Environment use "```vagrant destroy```" within the "```cmd```" prompt (Windows) or terminal (Linux/OSX)

4. To use the Development Environment use "```vagrant ssh```" (to connect into the VM) and "```sudo su```" (to obtain ROOT access) within the "```cmd```" prompt (Windows) or terminal (Linux/OSX)
