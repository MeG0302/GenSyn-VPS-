# GenSyn-VPS NODE

🚀 Gensyn Node Installer Setup for VPS
Welcome to the Gensyn Testnet Node installer!
This script and guide automate most of the setup, making it easier to get your Gensyn node online quickly mainly for VPS 

FOLLOW MeG here https://x.com/Jaishiva0302


SPECIAL CREDITS GOES TO https://x.com/Zun2025





🛠️ Prerequisites
VPS or server with:

Ubuntu 20.04, 22.04, or 24.04

(2-4)+ CPUs

8 GB RAM ( 20GB RECOMANDED for better results )

100+ GB SSD Storage


Buy any of these VPS 
here - https://contabo.com/en/vps/


![Screenshot 2025-04-27 211323](https://github.com/user-attachments/assets/0674d5b8-30be-446e-b40a-cf26522ba06b)


⚡ STEP-BY-STEP MANUAL INSTALLATION
Follow these steps to install your Gensyn Node manually:

1. Server Update
```bash
apt update && apt install -y sudo

 ```
2. Install Required Packages
```bash
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl wget screen git lsof nano unzip iproute2
```
3. NPM Installation and NPM 
```bash
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
```
4. Create screen session 
```bash
screen -S gensyn
```

5. Create tmux session 
```bash
tmux
```
6. Run the Node
```bash
cd $HOME && rm -rf gensyn-testnet && git clone https://github.com/zunxbt/gensyn-testnet.git && chmod +x gensyn-testnet/gensyn.sh && ./gensyn-testnet/gensyn.sh
```
.
.
.
.
.
.

Would you like to connect to the Testnet? [Y/n] 

>>> Press Y to join testnet


[][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][]

Which swarm would you like to join (Math (A) or Math Hard (B))? [A/b] 
>>> We have two type of Swarms:
A: Math (GSM8K dataset) -- Lower systems (>8GB) -- Use Small model (0.5B or 1.5B) for it.
B: Math Hard (DAPO-Math 17K dataset) -- Higher systems -- Use Big model (7B, 32B or 72B) for it.
How many parameters (in billions)? [0.5, 1.5, 7, 32, 72] >>> 0.5 is minimal and 72 is very big model. Choose based on your system.


AS FOR NOW CHOOSE OPTION "A" THEN "0.5B"

[][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][][]

.
.
.
.
.
.

Now we are moving on to the most important part, which is crucial for maximizing node uptime.
There is a “RAN OUT OF INPUT” issue on the VPS because the hardware isn’t powerful enough for AI training.
To address this, we will add a script that will help us maximize the node’s uptime.
Please follow the steps carefully.

like here  

![photo_2025-04-27_20-24-18](https://github.com/user-attachments/assets/a47a0930-ab61-46a7-b181-757fdde343cf)




I HAVE MADE A UPDATED SCRIPT IN ORDER TO FIX THIS PROBLEM

FIRST OF ALL STOP THE NODE BY PRESSING = CTRL+C

1) Script creation
```
 nano restart.sh

```
3) paste this 
```
#!/bin/bash
while true; do
    printf "1\na\n0.5\nn\n" | ./gensyn-testnet/gensyn.sh
    echo "Process crashed or stopped. Restarting in 30 seconds..."
    sleep 30
done

```

![Screenshot 2025-04-27 200206](https://github.com/user-attachments/assets/724402f3-5501-4dd5-b84d-67ebc3bb2d24)

then CTRL X then Y enter to save it

3) Give permission
```
chmod +x restart.sh
```
4) Start
```
./restart.sh
```

Now, your script is ready  
and every time your node stops or shut down due to any problem it will restart in 30 sec. no involvemnt is required  

MAKE SURE TO FOLLOW - https://x.com/Jaishiva0302
