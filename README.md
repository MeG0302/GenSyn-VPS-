# GenSyn-VPS NODE

🚀 Gensyn Node Auto-Installer Script
Welcome to the Gensyn Testnet Node installer!
This script and guide automate most of the setup, making it easier to get your Gensyn node online quickly.

FOLLOW MeG here https://x.com/Jaishiva0302


SPECIAL CREDITS GOES TO https://x.com/Zun2025


![Screenshot 2025-04-27 211323](https://github.com/user-attachments/assets/0674d5b8-30be-446e-b40a-cf26522ba06b)




🛠️ Prerequisites
VPS or server with:

Ubuntu 20.04, 22.04, or 24.04

4+ CPUs

16+ GB RAM ( 20GB RECOMANDED )

100+ GB SSD Storage

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
4. Create tmux session 
```bash
tmux
```
5. Run the Node
```bash
cd $HOME && rm -rf gensyn-testnet && git clone https://github.com/zunxbt/gensyn-testnet.git && chmod +x gensyn-testnet/gensyn.sh && ./gensyn-testnet/gensyn.sh
```bash
```
