# Kali Linux

## Install Kali-Linux on Windows 10 Sub Linux System

### Install xfce4 on kali linux over wsl in windows 10

```sh
wget https://kali.sh/xfce4.sh
cat xfce4.sh
sudo sh xfce4.sh
# above commands installed xfce4 and configured xrdp to listen on port 3390 but not start the service yet
# sudo apt-get install xrdp
sudo /etc/init.d/xrdp start

```

### Install Kali Linux Metapackages

Kali Linux provide multiple metapackages that would allow us to easily install subsets of tools based on particular needs.
https://www.kali.org/news/kali-linux-metapackages/

```sh
sudo apt-get install kali-linux
sudo apt-cache show kali-linux-top10

```

### Install metasploit

```sh
apt-get update
apt-get install metasploit-framework
```

