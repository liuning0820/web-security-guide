# Kali Linux

## Install xfce4 on kali linux over wsl in windows 10

```sh
wget https://kali.sh/xfce4.sh
cat xfce4.sh
sh xfce4.sh
# above commands installed xfce4 and configured xrdp to listen on port 3390 but not start the service yet
sudo /etc/init.d/xrdp start

```

## Install metasploit

```sh
apt-get update
apt-get install metasploit-framework
```