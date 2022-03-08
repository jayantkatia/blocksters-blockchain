# Blocksters

## Installation
1. Install WSL2 for windows users (Preferrably Debian or Ubuntu)
    1. Enable ```Windows Virtual Machine Platform``` and ```Windows Subsystem for Linux``` by typing ```Turn Windows Features``` in start search bar. System will ask to reboot, do Reboot.
    2. In Powershell, set ```wsl --set-default-version 2```
    3. Head to Microsoft store and download Debain or Ubuntu. \[OR\] run ```wsl --install -d <DistroName>``` in Powershell.
2. Install build-essential, golang, python, nodejs, curl, jq, docker and docker-compose 
```
sudo apt-get install build-essential curl golang python nodejs docker docker-compose jq
```
3. Run ```curl -sSL https://bit.ly/2ysbOFE | bash -s```
4. Add ```export PATH="<path_to_3rd_step_downloaded_directory_bin>:$PATH"``` to ```~/.bashrc``` file at the bottom.
5. Git clone this repo, ```cd``` into it and run ```./fablo up``` 