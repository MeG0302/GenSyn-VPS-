>[!Note]
This is the guide for updating your gensyn node.

if you are looking for node running guide you may check here - https://github.com/MeG0302/GenSyn-VPS-/

### Many people are facing "Bootstrap_timeout" issue with gensyn node 
![photo_2025-05-05_17-04-57](https://github.com/user-attachments/assets/06140a2c-1417-4c56-8fe2-6f4bf8fc9710)
> if you also then simply follow the steps listed below one by one 


### 1. Stop the previous node session first.
press ctrl c to stop the process 
### or if it is not shutting down then simply kill the screen session 
```
pkill -f "SCREEN.*gensyn"
```
then create a new screen 
```
screen -S gensyn
```
### 2. Delete exisiting temp-data

```
[ -n "$(ls "$HOME/rl-swarm/modal-login/temp-data/"*.json 2>/dev/null)" ] && rm -f "$HOME/rl-swarm/modal-login/temp-data/"*.json 2>/dev/null || true

```

### 3. Use this command to run the `rl-swarm`
```
cd $HOME && rm -rf gensyn-testnet && git clone https://github.com/zunxbt/gensyn-testnet.git && chmod +x gensyn-testnet/gensyn.sh && ./gensyn-testnet/gensyn.sh
```
- After running this command, it will ask for your choice and you need to press 1 (use existing `swarm.pem` file) :
  
![Screenshot 2025-05-05 171422](https://github.com/user-attachments/assets/eefe6b7f-3990-49b1-b25d-e0a968653c9f)


- LOG IN with the same email (for the same swarm.pem)


press "N" when it ask you ```Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N]``` here Write `N` 

### 4. Configuration
> # Press "A" to select (MATH) then type "0.5" if you are running in vps (to avoid any failure)

### 5. Normal logs
> these are the normal logs after which you can detach from the screen 
#
![Screenshot 2025-05-05 172337](https://github.com/user-attachments/assets/18edbbb8-ead3-4cae-ab65-19bb45ebcf83)


### 6. Detach from this screen session
- Use `Ctrl + A` and then press `D` to detach from this screen session.


#
#
#
#

## NOTE 
Even after successful installation you still see your EOA address as 0x0000000000000000.............

then 
### STOP NODE
> repeat step 1 and 2 then paste this command 

```
pkill -f rl-swarm

```

>> caution : Dont use this command if you are running other nodes in this vps aswell.


After that repeat whole step after step 3 
it will definately work

