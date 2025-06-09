# Free Home SIEM

In an effort to gain a deeper understanding of SOC infrastructure, I decided to set up a simple SIEM. This has been done using a Raspberry Pi, some virtual machines (using virtual box) and Wazuh. As described on their site "Wazuh is a free and open source security platform that unifies XDR and SIEM capabilities. It protects workloads across on-premises, virtualized, containerized, and cloud-based environments." This means i was able to deploy all of this for the free!!

### Tools Used:
1. [Wazuh](https://wazuh.com/)
2. [Virtual box](https://www.virtualbox.org/)
3. [Ubuntu](https://ubuntu.com/)

The Raspberry pi I already had and just used RaspberryPi OS. So I technically did not have to purchase anyhting for this project. The Pi was used as the Wazuh Server as I had a 256gb SD card so storage will not be an issue. I'm limited in how many VMs i can run at once as my laptop only has 8GB :(. 

## I need a Wazuh server

This is going to be the raspberry Pi, the specs are a bit low for it, but, somehow it worked. You can find the system requirements [here](https://documentation.wazuh.com/current/quickstart.html)

To install this on to the raspberry pi I needed to ssh on to it and run the following command:

```curl -sO https://packages.wazuh.com/4.12/wazuh-install.sh && sudo bash ./wazuh-install.sh -a```

This will take quite some time, so don't be alarmed by this. Once it does complete, you will be given an address to the server, which will be something like ```https://xxx.xxx.xxx.xxx:443```, then you will be brough to the following page: 

<img width="1140" alt="Screenshot 2025-06-09 at 21 23 27" src="https://github.com/user-attachments/assets/16a35d42-cff4-4e9c-be0d-87592c65a999" />


