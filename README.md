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

## Fix clock for dualboot Linux-Windows
1. Start Windows and execute Registry Editor `regedit`.
2. Navigate to the following path inside the registry editor:
```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\TimeZoneInformation
```
3. Right-click to create a New DWORD (32-bit) with name `RealTimeIsUniversal`.
4. Double-click over `RealTimeIsUniversal` file and set value data to 1 and click "OK" to save.

## Recommended software list

| Software type     | Windows                 | Linux                          |
| :---------------: | :---------------------: | :----------------------------: |
| **Archivers**     | 7zip                    | p7zip-full                     |
|                   | winrar                  | p7zip-full + p7zip-rar + unrar |
|                   | winzip                  | p7zip-full                     |
| **Cloud**         | dropbox                 | dropbox                        |
|                   | google-drive            | -                              |
|                   | google-file-stream      | -                              |
| **Development**   | mingw                   | g++ / gcc                      |
|                   | git                     | git-core                       |
|                   | github-desktop          | -                              |
| **Downloads**     | clipgrab                | clipgrab                       |
|                   | μtorrent                | deluge                         |
| **Graphics**      | lightshot               | flameshot                      |
|                   | photoshop               | gimp                           |
|                   | paint                   | gnome-paint                    |
| **Multimedia**    | camera                  | cheese                         |
|                   | groove-music            | cmus / rhythmbox               |
|                   | movies-&-tv             | gnome-player / vlc             |
| **Office**        | microsoft-office        | libre-office                   |
|                   | pdfchain                | pdfchain                       |
|                   | wps-office              | wps-office                     |
| **System**        | windows-disk-management | gparted                        |
