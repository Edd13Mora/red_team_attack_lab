# TODO LIST
- [ ] Clean up Configs
  - [x] Vagrant configs
    - [x] Use proper inventory
      - REF: https://github.com/jborean93/ansible-windows/blob/master/vagrant/Vagrantfile
      - REF: https://github.com/jborean93/ansible-windows/blob/master/vagrant/inventory.yml
    - [x] Potentially figure out dynamic way to do WinRM port forwarding instead of static/semi-static
      - Cleaned this up to an acceptable level
  - [ ] Base Ansible configuration values in one place
- [x] Clean up red_team_attack_lab.py
    - [x] FIX: can't run the range from any path due to config reading, but updating the config reading breaks the VagrantController reading the vagrant files due to bad path handling as well
- [x] Automate ADCS deployment
  - [x] Automate ADCS Certificate Authority
  - [x] Automate ADCS Enrollment Web Service
  - [x] Automate ADCS Web Enrollment
- [x] Dynamic domain name
    - [x] default to "attacklab.local"
    - [x] Ensure proper usage of config variables so we only have to change it in one location
- [ ] Change domain admin username to "Admin"
    - [ ] Ensure proper usage of config variables so we only have to change it in one location
- [ ] Ensure local administrator account is properly created seperate from DA Admin account
- [ ] Automatically remove hosts from AD on `vagrant destroy`
    - REF: https://www.vagrantup.com/docs/triggers/usage
    - REF: https://docs.ansible.com/ansible/latest/collections/community/windows/win_domain_computer_module.html#parameter-state
    - REF: https://stackoverflow.com/questions/40087032/how-to-run-a-vagrant-task-on-vagrant-destroy
- [ ] Add documentation
    - [x] Installation
    - [ ] Default credentials & config variables
    - [x] How to get running
    - [ ] Debugging commands
    - [ ] How to add/update/test/add stuff
      - [ ] Common pitfalls
    - [ ] Lab architecture diagram
    - [ ] Existing AD vulnerabilities
      - /docs/vulns?
    - [ ] FAQ
- [ ] Add attack walkthroughs
    - [ ] /docs/vulns/walkthroughs folder?
- [ ] Add more AD vulns
  - [ ] Look into DSC?
    - REF: https://docs.ansible.com/ansible/latest/user_guide/windows_dsc.html
- [ ] Make Ansible faster
  - REF: https://docs.ansible.com/ansible/latest/user_guide/playbooks_async.html
  - REF: https://docs.ansible.com/ansible/latest/user_guide/playbooks_strategies.html
- [x] Make Vagrant faster
  - REF: https://www.vagrantup.com/docs/providers/virtualbox/configuration#linked-clones
- [ ] Improve Windows QoL with scripts
    - [ ] Steal from DetectionLab
- [ ] Add hosts
    - [ ] [Metasploitable 3](https://github.com/rapid7/metasploitable3)
      - [ ] Windows
      - [ ] Ubuntu
    - [ ] Server 2008
      - [jborean93/WindowsServer2008-x86](https://app.vagrantup.com/jborean93/boxes/WindowsServer2008-x86)
      - [jborean93/WindowsServer2008-x64](https://app.vagrantup.com/jborean93/boxes/WindowsServer2008-x64)
      - [jborean93/WindowsServer2008R2](https://app.vagrantup.com/jborean93/boxes/WindowsServer2008R2)
    - [ ] Server 2012
      - [jborean93/WindowsServer2012](https://app.vagrantup.com/jborean93/boxes/WindowsServer2012)
      - [jborean93/WindowsServer2012R2](https://app.vagrantup.com/jborean93/boxes/WindowsServer2012R2)
    - [ ] Server 2016
      - [StefanScherer/windows_2016](https://app.vagrantup.com/StefanScherer/boxes/windows_2016)
    - [ ] Server 2022
      - [StefanScherer/windows_2022](https://app.vagrantup.com/StefanScherer/boxes/windows_2022)
    - [x] Windows 7
      - [d1vious/windows_7](https://app.vagrantup.com/d1vious/boxes/windows_7)
    - [ ] Ubuntu Server 20
    - [ ] Ubuntu Server 18
    - [ ] Ubuntu Desktop 20
    - [ ] Ubuntu Desktop 18
    - [ ] CentOS ?