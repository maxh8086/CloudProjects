JenkinMaster-Slave-Setup-ARM-Template.json has been prepared to setup Jenkins Master server with 1 Slave VM.

This ARM Template will Deploy below setup in ResourceGroup under same Location as ResourceGroup:
- 1 vNet and 1 Subnet.
- 1 Jenkins Master VM with NIC
    - 1 Public IP with DNS Registration
    - 1 NSG with rule to allow 8080/Tcp and 22/Tcp
- 1 Ubuntu VM with NIC
    - 1 Public IP
    - 1 NSG with port 22/Tcp
    - private key for jenkins slave ssh authentication will be available at /home/jenkins/.ssh/id_rsa