# Temple HPC Facility Configuration
![My Remote Image](https://www.giving.temple.edu/s/705/images/editor/1_giving_site/fye2020/thumb/cst_formal_red_black_600.jpg)

## Resources
- 16 CPU cores and 
- 512GB of RAM, and 
- 4x NVIDIA Tesla V100 GPUs interconnected with NVlink2.
- VRAM for each GPU is 16, totaling  16x4 VRAM
- Accessible from anywhere via SSH


## Application Process

To gain access to the High-Performance Computing (HPC) resources provided by Temple University, you can follow these steps:

- Visit the HPC website at https://www.hpc.temple.edu/.
- Choose the appropriate option based on your needs, such as machine learning, computing, or owl nest. Each option offers different features and criteria.
- Click on "Request Access."
- Specify your requirements, including your field, a description of your project, resource requirements, required software, and your supervisor's name.
- Read and agree to the terms and conditions.
- After submitting your request, your documents will be reviewed, and you should receive access within 2 to 3 business days.


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