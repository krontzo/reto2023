# reto2023
Challenge 2023 - Team 3 @ Cinvestav

## Requirements

- Asus Xtion sensor
- Ubuntu 22.04.1 LTS amd64


## Ubuntu

This section lists the Ubuntu 22.04.1 LTS installation steps, for the required software.

Open terminal with Ctrl-Alt-t and enter the commands line by line

```bash
sudo ufw enable
sudo apt update -y
sudo apt upgrade -y
sudo apt install -y git cmake build-essential
sudo apt install -y libopencv-dev libopenni2-dev libpcl-dev openni2-utils
sudo apt install -y vim-gtk3 tmux ripgrep neofetch 7zip bat brotli curl fzf ipython3 mpv yt-dlp universal-ctags tig darknet qt6-base-dev
cd ~/Documents/
git clone --depth 1 --branch qt5 https://github.com/krontzo/recording_openni2_primesense.git grabar
cd ~/Documents/grabar/
cmake -B build -S . && cmake --build build/
cd ~/Documents/
git clone https://github.com/krontzo/label_qt6.git etiquetar
cd ~/Documents/etiquetar/
mkdir build && cd build && qmake6 .. && make
mkdir -p ~/Documents/basededatos
cd ~/Documents/basededatos
~/Documents/grabar/bin/viewer &
~/Documents/etiquetar/build/YoloLabel &
```


## CoppeliaSim Edu

Use the link <https://www.coppeliarobotics.com/files/CoppeliaSim_Edu_V4_4_0_rev0_Ubuntu22_04.tar.xz>


```bash
cd ~/Downloads/
curl -O "https://www.coppeliarobotics.com/files/CoppeliaSim_Edu_V4_4_0_rev0_Ubuntu22_04.tar.xz"
```
