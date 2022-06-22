# ubuntu
clear, update




Removing old Kernels (to free space on /boot) see: http://askubuntu.com/questions/89710/how-do-i-free-up-more-space-in-boot

```bash
sudo apt-get purge $(dpkg -l linux-{image,headers}-"[0-9]*" | awk '/ii/{print $2}' | grep -ve "$(uname -r | sed -r 's/-[a-z]+//')")
```

Then run


    sudo apt-get update

