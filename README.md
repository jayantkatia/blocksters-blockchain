# Blocksters

## Installation
1. Install WSL2 for windows users (Preferrably Debian)
    1. Enable ```Windows Virtual Machine Platform``` and ```Windows Subsystem for Linux``` by typing ```Turn Windows Features``` in start search bar. System will ask to reboot, do Reboot.
    2. In Powershell, set ```wsl --set-default-version 2```
    3. Head to Microsoft store and download Debain. \[OR\] run ```wsl --install -d <DistroName>``` in Powershell.
2. Install build-essential, golang, python, nodejs, curl, jq, wget, docker and docker-compose 
```
sudo apt-get install build-essential curl wget golang python nodejs docker docker-compose jq
```
3. According to [this](https://github.com/microsoft/WSL/discussions/4872#discussioncomment-99164), Run
```
sudo touch /etc/fstab
sudo update-alternatives --set iptables /usr/sbin/iptables-legacy
sudo update-alternatives --set ip6tables /usr/sbin/ip6tables-legacy
sudo service docker start
service docker status
````
4. Run ```curl -sSL https://bit.ly/2ysbOFE | bash -s```
5. Add ```export PATH="<path_to_3rd_step_downloaded_directory_bin>:$PATH"``` to ```~/.bashrc``` file at the bottom.
6. Git clone this repo, ```cd``` into it and run ```./fablo up``` 

## Development

1. Up the network using ```./fablo up```
2. After changing fablo-config.json, run ```./fablo recreate```