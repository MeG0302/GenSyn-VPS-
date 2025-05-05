>[!Note]
>Whenever Gensyn updates their node, use these commands one by one. However, wait for my update before proceeding. Join my Telegram channel to get the latest information when an update is needed : [ZunXBT](https://t.me/zunxbt)

### 1. First kill all the existing gensyn screen session
```
pkill -f "SCREEN.*gensyn"
```
### 2. Create a screen session named `gensyn`
```
screen -S gensyn
```
### 3. Delete exisiting temp-data
```
[ -n "$(ls "$HOME/rl-swarm/modal-login/temp-data/"*.json 2>/dev/null)" ] && rm -f "$HOME/rl-swarm/modal-login/temp-data/"*.json 2>/dev/null || true
```
### 4. Now use this command to run the `rl-swarm`
```
cd $HOME && rm -rf gensyn-testnet && git clone https://github.com/zunxbt/gensyn-testnet.git && chmod +x gensyn-testnet/gensyn.sh && ./gensyn-testnet/gensyn.sh
```
- After running the above command, it will show something like this :
  
![Screenshot 2025-04-21 075405](https://github.com/user-attachments/assets/37d28590-6f4f-4ecd-9cb6-c831a821e400)

- You should choose 1 to use existing `swarm.pem` file
>[!Note]
> It will ask this question - ```Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N]``` here Write `N` and at last you will see this : ```Your training session is about to begin``` then you can detach from this gensyn screen session

### 5. Detach from this screen session
- Use `Ctrl + A` and then press `D` to detach from this screen session.
