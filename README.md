# ansible-hands-on
Ansible Handson Tutorial

## Installation Steps

- Virtual Box Install
- Go to https://www.osboxes.org/centos/
- 64 Bit Machine
- Unzip the download
- You will have vdi in it
- Go to Virtual Box Application
    - create new
    - centos-template
    - Type: Linux
    - Version: Other 64 Bit
    - Next
    - Select Memory - 1GB
    - Hard Disk - Use the VDI Downloaded - Use and Existing
    - Network - Adapter 1 to Bridge Network - It will get it own IP and also can connect to internet of Host
    - Username and Password on osboxes.org site Info Tab from where it was downloaded
    - Start the centos-template machine
    - Get the IP by going to terminal - ifconfig
    - Go to your Host machine
    - Use terminal for ssh to the IP of centos-template - `ssh <username>@<ip-of-centos-template>`

- As we want to test this on multiple machine we need to clone the template machine, we will be having three machine - one master and two slave
    - Close the centos-template machine which is running
    - Right Click and Clone  
        - Expert Mode
        - name it as ansible-controller
        - select Generate new MAC address for all network adapters
        - select Linked Clone
    - Do the same steps for creating ansible-target1 and ansible-target2
    - We need to rename the three machine  
        - For ansible controller
        - `sudo vi /etc/hostname`
        - make it ansiblecontroller from osboxes
        - save the file
        - `sudo vi /etc/hosts`
        - update the entry of 127.0.0.1 localhost ansiblecontroller and ::1 localhost ansiblecontroller
        - save the file
        - restart the system so as these above changes are updated
        - Do the similar changes for other machine as well and make target1 and target2
       
- We need to install ansible on controller machine
    - `sudo yum install ansible`
    - To check whether ansible is installed properly `ansible --version`
    
