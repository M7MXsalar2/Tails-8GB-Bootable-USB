# Tails 8GB USB flash drive bypass

Flash tails `.img` to any size flash drive *(less than 8GB)*.  
Plug in USB to any machine with gdisk  
Move GTP backup data to the end of the disk and generate new UUIDS: 

```sh
gdisk /dev/sdX
# Expert Mode
x
# Move GPT backup data structures to the end of the disk
e
# Generate new random Partition and Disk UUIDS:
c R
g R
w
YES
```
