# SSH-VM-TUTO

This tutorial explains how to connect to a VM via SSH from a terminal and Visual Studio Code. This can be useful for working inside a VM from your local computer.

## Configuring your VM

To be able to connect to your VM via SSH, you must first enable the SSH server on your VM. Follow these steps to do so:

1. Open the settings for your VM and enable file sharing and the SSH port. You should have something similar to this:

![portssh](https://user-images.githubusercontent.com/46847941/150156747-ccfd58ab-b8d9-45ab-af08-ed90ac329026.png)

2. In the terminal of your VM, add your user to the `sudo` group with the following command:
-
  ```
  sudo usermod -aG sudo {loginVM}
3. Install the openssh-server and ssh packages with the following commands:
-
  ```
  sudo apt-get install openssh-server ssh
## Connecting from a terminal
-
  ```
  ssh -p 3022 {loginVM}@127.0.0.1
## Connecting from Visual Studio Code
To connect to your VM via SSH from Visual Studio Code, follow these steps:

- Install the "Remote - SSH" extension from the Visual Studio Code marketplace.
- Click on the "Remote" icon in the sidebar and select "Add New SSH Host...".
- Enter the following connection information:
  - Address: ssh -p 3022 {loginVM}@127.0.0.1
  - Password: the password for your VM
<img width="252" alt="Screen Shot 2022-01-19 at 4 05 52 PM" src="https://user-images.githubusercontent.com/46847941/150157638-11b84507-16a9-43c2-aa1c-4a641d10ed30.png">
 
<br />
 
- If you don't have editing privileges  
  
    ```
    sudo chmod -R 755 .
- Error: kex_exchange_identification: Connection closed by remote host  
  
  ```
  sudo service ssh start
