# My Linux Configuration
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
    export https_proxy="https://proxy4.unal.edu.co:8080"
    export socks_proxy="https://proxy4.unal.edu.co:8080"
    export gopher_proxy="https://proxy4.unal.edu.co:8080"
    export ftp_proxy="https://proxy4.unal.edu.co:8080"
    export http_proxy="https://proxy4.unal.edu.co:8080"
    export no_proxy="https://proxy4.unal.edu.co:8080"
    export ssh="https://proxy4.unal.edu.co:8080"
}
```
3. Run to apply the proxy configurations
```
unproxycli
```

## Recommended software list

| Software type     | Linux                | Windows                         |
| :---------------: | :------------------: | :-----------------------------: |
| **Archivers**     | p7zip-full           | winzip, 7zip                    |
|                   | p7zip-rar            | winrar                          |
|                   | unrar                | winrar                          |
| **Cloud**         | dropbox              | dropbox                         |
|                   | -                    | google-drive                    |
|                   | -                    | google-file-stream              |
| **Development**   | default-jdk          | jdk                             |
|                   | g++                  | mingw                           | 
|                   | gcc                  | mingw                           |
|                   | git-core             | git/git-desktop                 | 
|                   | nodejs               | nodejs                          |
|                   | python               | python                          |
| **Downloads**     | clipgrab             | clipgrab                        |
|                   | deluge               | deluge                          |
| **Graphics**      | flameshot            | lightshot                       |
|                   | gimp                 | gimp/photoshop                  |
|                   | gnome-paint          | paint                           |
| **IDE**           | codeblocks           | codeblocks                      |
|                   | eclipse              | eclipse                         |
|                   | idle3                | idle3                           |
|                   | visual-studio-code   | visual-studio-code              |
| **Multimedia**    | cheese               | camera                          |
|                   | gnome-mplayer        | movies-&-tv                     |
|                   | rhythmbox            | winamp                          |
|                   | vlc                  | movies-&-tv                     |
| **Office**        | libre-office         | microsoft-office                |
|                   | pdfchain             | adobe-acrobat-dc                |
|                   | wps-office           | microsoft-office                |
| **System**        | gparted              | windows-disk-management         |
