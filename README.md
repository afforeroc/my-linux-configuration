# My Linux Configurations
Using terminal

## Only for Debian
1. Open 'sources.list' with nano for edit
```
nano /etc/apt/sources.list
````
2. Copy and paste the following lines at the end of file 'sources.list' and save it
```
deb http://security.debian.org/ stable/updates main contrib non-free
deb-src http://security.debian.org/ stable/updates main contrib non-free
deb http://ftp.debian.org/debian/ stable main contrib non-free
deb-src http://ftp.debian.org/debian/ stable main contrib non-free
```
## Basic configurations
1. Update and upgrade all operative system
```
sudo apt update && sudo apt upgrade && sudo apt dist-upgrade
sudo apt autoremove && sudo apt autoclean
```

2. Install basic software 
```
sudo apt-get install p7zip-full p7zip-rar unrar gparted ntfs-3g
```

3. Install some package with '.deb' extension
```
sudo dpkg -i package_example.deb
```

## Proxy configuration
1. Open '~/.bashrc' with nano for edit
```
nano ~/.bashrc 
```

2. Copy and paste the following lines at the end of file 'bashrc' and save it
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
3. Run to apply the proxy configurations
```
unproxycli
```

## Recommended software list

| Software          | Linux                | Windows             |
| :---------------: | :------------------: | :-----------------: |
| **Archivers**     | p7zip-full           | 7zip                |
|                   | p7zip-rar            | 7zip/winrar         |
|                   | unrar                | winrar              |
| **Astronomy**     | celestia             | //                  |
|                   | stellarium           | //                  |
|                   | <no alternative>     | worldwide-telescope |
| **Browsers**      | firefox              | //                  |
|                   | google-chrome        | //                  |
| **Cloud**         | dropbox              | //                  |
|                   | <no alternative>     | google-drive        |
|                   | <no alternative>     | google-file-stream  |
| **Development**   | default-jdk          | jdk                 |
|                   | g++                  | mingw               |
|                   | gcc                  | cygwin              |
|                   | git-core             | git                 |
|                   | nodejs               | //                  |
|                   | python3              | //                  |
| **Downloads**     | clipgrab             | //                  |
|                   | deluge               | //                  |
| **Graphics**      | flameshot            | lightshot           |
|                   | gimp                 | //                  |
|                   | gnome-paint          | paint               |
| **IDE**           | codeblocks           | //                  |
|                   | eclipse              | //                  |
|                   | geany                | //                  |
|                   | idle3                | //                  |
|                   | visual-studio-code   | //                  |
| **Multimedia**    | cheese               | <whatever>          |
|                   | gnome-mplayer        | gom-player          |
| **Office**        | libre-office         | microsoft-office    |
|                   | pdfchain             | adobe-acrobat       |
|                   | wps-office           | //                  |
| **Videogames**    | gfceu                | //                  |
|                   | gnome-games          | <whatever>          |
|                   | pcsxr                | //                  |
