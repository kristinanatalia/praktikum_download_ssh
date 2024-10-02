
Nama: kristina natalia hutauruk
Nim: 09011282328120
Kelas: sk3c

**Step 1: atur jaringan**
![Network Settings 1](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/Screenshot%20(337).png)
![Network Settings 2](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/Screenshot%20(338).png)

**step 2**
![Network Configuration](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/Screenshot%20(339).png)
 
**Step 3: Install SSH on Ubuntu**
OpenSSH is not pre-installed on the system, so let's install it manually. To do this, type in the terminal:
**sudo apt install openssh-server**
The installation of all the necessary components will begin. Answer "Yes" to all the system prompts. 
After the installation is complete, go to the next step to start the service.
![SSH Installation](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/1.png)
 
**Step 4: Start SSH**
Now you need to enable the service you just installed using the command below:
**sudo systemctl enable --now ssh**
![Enable SSH](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/2.png)
On successful startup, you will see the following system message.
The **--now** key helps you launch the service and simultaneously set it to start when the system boots.
To verify that the service is enabled and running successfully, type:
**sudo systemctl status ssh**
The output should contain the **Active: active (running)** line, which indicates that the service is successfully running.
If you want to disable the service, execute: 
![SSH Status](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/3.png)

**sudo systemctl disable ssh**
It disables the service and prevents it from starting at boot.
![Disable SSH](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/4.png)
 
**Step 5: Configure the firewall**
Before connecting to the server via SSH, check the firewall to ensure it is configured correctly.
In our case, we have the UFW installed, so we will use the following command:
**sudo ufw status**
In the output, you should see that SSH traffic is allowed. If you don't have it listed, you need to allow incoming SSH connections. This command will help with this:
**sudo ufw allow ssh**
![Firewall Configuration](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/4.png)

**Step 5: Connect to the server**
Once you complete all the previous steps, you can log into the server using the SSH protocol.
To do this, you will need the server's IP address or domain name and the name of a user created on the server.
In the terminal line, enter the command:
**ssh username@IP_address**
![SSH Connection](https://raw.githubusercontent.com/kristinanatalia/praktikum_download_ssh/main/6.png)
