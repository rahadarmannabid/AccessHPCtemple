# Temple HPC Facility Configuration

## Resources
- 16 CPU cores and 
- 512GB of RAM, and 
- 4x NVIDIA Tesla V100 GPUs interconnected with NVlink2.
- VRAM for each GPU is 16, totaling  16x4 VRAM
- Accessible from anywhere via SSH


## Application Process

- Step1: Go to https://www.hpc.temple.edu/ 
- Step 2: Apply for machine learning or compute or owl nest depending upon your need, all the criteria give different types of features.
- Step 3:Select Request Access
- Step 4:Specify your needs e.g.-  filed, description, Resource Requirements, Software, supervisor
- Step 5: Agree with their terms and conditions
- Step 6: Within 2/3 business days they will give access after reviewing your documents.



## How to access it from your computer?

- Access via vscode:
    - The best way I found to access HPC is from VS code.
    - Install an extension called “Remote- SSH”
    - Click on the Remote- SSH extension and write- 
    ```
    ssh accessnetid@gpu.hpc.temple.edu
    ```
- Access via Jupyter Nodebook:
    - From the VSCode terminal create: python3 -m venv env (In the base environment, you don’t have any access to install any package. You need to create a new environment.)
    - To install Anaconda write the command: : 
    ```
    wget https://repo.anaconda.com/archive/Anaconda3-2020.07-Linux-x86_64.sh
    ```

    ```
    bash Anaconda3-2020.07-Linux-x86_64.sh
    ```
    - To install jupyer notebook write the command  (it will take time to fix some dependencies): 
    ```
    conda install jupyter notebook
    ```
    - If you want to run the jupyter notebook write cmd: 
    - Copy the token (ex: http://127.0.0.1:8889/?token=22dd2ab63c90249bf4fa3da5ba468f5ceb034f64ff04)  and paste in your browser. Here you go!!

## Accessing HPC computer WITHOUT passward: 
- On your Mac or Linux PC, open up your terminal and run the following command (unless you already have an .ssh/config file.)
    ```
    touch ~/.ssh/config
    ```
- you will see files in your .ssh folder. E.g: config, id_rsa, id_rsa.pub

- Use nano or any text editor you prefer to copy and paste the following in the config file. Of course replace your User name with your AccessNet name.
    ```
    Host Temple-GPU-4
    # ssh tuq24452@gpu.hpc.temple.edu
    HostName 129.32.84.168
    User tuq24452
    Port 22
    ```
- Create SSH Key in your local computer and add it to each server's id_rsa file.
    - This cmd will create new key:
        ```
        ssh-keygen
        ```
    - Then press enter to save the key into id_rsa.pub 
- Here we go. We don't need to put passward each time. 


## Written by:

[Rahad Arman Nabid](https://rahadarmannabid.github.io/rahadarmannabid/index.html)

