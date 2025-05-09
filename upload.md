# UPLOAD SWARM.PEM FROM YOUR LOCAL PC TO YOUR VPS/GPU

### STEP 1
upload your swarm.pem file into -> https://tmpfiles.org/

### STEP 2 
copy the link generated there and paste it somewhere

![Screenshot 2025-05-06 024112](https://github.com/user-attachments/assets/3fcfb09c-cbc8-474f-8aa9-eeebdc6e3a44)

### STEP 3
Complete whole process of node run (also use the same email you just uploaded swarm.pem file[previous login data])
https://github.com/MeG0302/GenSyn-VPS-/

### STEP 4
Stop the current node with ctrl C then delete the previous swarm.pem from the rl-swarm folder before preceeding 
```
# 1. Make sure the rl-swarm directory exists and you're in the right place
ls /root/rl-swarm
```
```
# 2. Delete the old swarm.pem file
rm /root/rl-swarm/swarm.pem

```


### STEP 4
Add "wget" before the link you saved and paste this code in your VPS/GPU

> example = 
```

wget https://tmpfiles.org/xxxxxx/swarm.pem


```


### STEP 5
move file to the rl-swarm folder 
```

# 3. Move the new file
mv swarm.pem /root/rl-swarm/


```

### STEP 6
Now complete the whole node installation as in the guide https://github.com/MeG0302/GenSyn-VPS-/

NOTE
> if you get any error you can siply paste this error in chat gpt to find solution.

 
### NOW YOU CAN RUN YOUR NODE 
