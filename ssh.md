# SSH on Mobian
Quick tutorial for setting up SSH from a Linux desktop to the Pinephone.

- Generate keys on your desktop: `ssh-keygen`
- Copy the key (id_rsa.pub) from desktop to mobile e.g using Syncthing or any other method. Add it as an authorized key on the phone:
```
mkdir ~/.ssh
chmod 700 ~/.ssh
cat ~/id_rsa.pub >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
chown -R mobian.mobian ~/.ssh
```

- Install `ip` on the phone (`sudo apt install iproute2`) to determine local IP address using `ip addr`.

- Install ssh server `sudo apt install openssh-server`.
- `sudo systemctl start ssh`
- Connect from desktop: `ssh mobian@LOCAL_IP_ADDRESS`
