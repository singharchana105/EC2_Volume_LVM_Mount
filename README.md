# Volume Mount

Step 1. In EC2 Add Some Volume From AWS Account.
Step 2. Now open the terminal connect it with ssh .
Step 3. run command - lsblk
Step 4. Run - lvm
Step 5. (Physical volume, volume group, logical volume create)
        - pvcreate /dev/xvdf [physical volume created]
         For preview Run - pvs command
         - vgcreate archu_vol /dev/xvdf [volume group created]
         - lvcreate -L +5G -n archu_logic archu_vol [logical volume of 5GB created]

Step 6. where to mount data we have to decide path . so generally mount data in mnt folder.
ls, cd mnt , mkdir vol

Step 7. logical volume extension has to be changed, so for that
**mkfs -t ext4 dev/archu_vol/log_vol(logical volume name hai)**

Step 8. mount  /dev/archu_vol/log_vol  /mnt/vol.

Step 9. df -h
         
        
