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
    - Use terminal for ssh to the IP of centos-template - ssh <username>@<ip-of-centos-template>
