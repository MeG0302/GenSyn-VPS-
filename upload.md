# UPLOAD SWARM.PEM FROM YOUR LOCAL PC TO YOUR VPS/GPU

### STEP 1
upload your swarm.pem file into -> https://tmpfiles.org/

### STEP 2 
copy the link generated there

![Screenshot 2025-05-06 024112](https://github.com/user-attachments/assets/3fcfb09c-cbc8-474f-8aa9-eeebdc6e3a44)


### STEP 3
add wget before the link and paste this code in your VPS/GPU

> example = 
```

wget https://tmpfiles.org/xxxxxx/swarm.pem


```
### STEP 3
Before moving swarm.pem you need to create rl-swarm folder and in order to make that folder just use this guide until login process (when you see login prompt in your terminal just stop the node using ctrl c)
https://github.com/MeG0302/GenSyn-VPS-/

### STEP 4
move file to the rl-swarm folder 
```


sudo mv swarm.pem /rl-swarm/


```

### STEP 5
Now complete the whole node installation as in the guide https://github.com/MeG0302/GenSyn-VPS-/

NOTE
> if you get any error you can siply paste this error in chat gpt to find solution.

 
### NOW YOU CAN RUN YOUR NODE 
