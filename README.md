# modern.ie-vagrant

##### Requirements

- VirtualBox
- Vagrant

Modern.ie for Vagrant 

To create a new Modern.IE box:
   * Clone this repository
   ```bash
   $ git clone https://github.com/hugsy/modern.ie-vagrant.git win8
   ```  
   * Edit `Vagrantfile` to change the line `VM = VMS[<id>]` where `id` is the index of the box you want to have (default: `Windows 8 / IE11`)
   * For the directory, launch Vagrant the first time with the environment `FIRSTBOOT` set to `1`
   ```bash
   $ cd win8 && FIRSTBOOT=1 vagrant up
   ```
   _NOTE_: the `FIRSTBOOT` will force Vagrant to show a GUI for the VM, which is required to run the initial scripts and enable WinRM
   
The next boot can be done without the `FIRSTBOOT` environment variable

To test an application running on port `4000` on the host, find the ip address of the host, in Ubuntu execute `ip address` and point your browser in the guest Windows machine to the ip address + port, i.e. `http://192.168.0.110:4000`
   
That's it!!
