# My Linux Configurations
Using terminal

## Only for Debian
* 1. Open 'sources.list' with nano for edit
```
nano /etc/apt/sources.list
````
* 2. Copy and paste the following lines at the end of file 'sources.list' and save it
```
deb http://security.debian.org/ stable/updates main contrib non-free
deb-src http://security.debian.org/ stable/updates main contrib non-free
deb http://ftp.debian.org/debian/ stable main contrib non-free
deb-src http://ftp.debian.org/debian/ stable main contrib non-free
```
## Basic configurations
* 1. Update and upgrade all operative system
```
sudo apt update && sudo apt upgrade && sudo apt dist-upgrade
sudo apt autoremove && sudo apt autoclean
```

* 2. Install basic software 
```
sudo apt-get install p7zip-full p7zip-rar unrar gparted ntfs-3g
```

* 3. Install some package with '.deb' extension
```
sudo dpkg -i package_example.deb
```

## Proxy configuration
* 1. Open '~/.bashrc' with nano for edit
```
nano ~/.bashrc 
```

* 2. Copy and paste the following lines at the end of file 'bashrc' and save it
```
unproxycli () {
    export https_proxy="https://168.176.239.41:8080"
    export socks_proxy="http://168.176.239.41:8080"
    export gopher_proxy="http://168.176.239.41:8080"
    export ftp_proxy="http://168.176.239.41:8080"
    export http_proxy="http://168.176.239.41:8080"
    export no_proxy="http://168.176.239.41:8080"
    export ssh="http://168.176.239.41:8080"
}
```

## Recommended software list
* 1. Browsers
- firefox
- google-chrome

* 2. Development
- codeblocks
- default-jdk
- eclipse
- g++ 
- gcc
- idle3
- pip3
- python3
- visual-studio-code

* 3. Downloads
- clipgrab
- deluge

* 3. Education 
- stellarium

* 4. File archivers
- p7zip-full
- p7zip-rar
- unrar

* 5. Graphics
- gimp
- gnome-paint

* 6. Multimedia
- cheese
- gnome-mplayer

* 7. Office
- libre-office
- pdfchain
- wps-office

* 8. Videogames
- gfceu
- gnome-games
- pcsxr
