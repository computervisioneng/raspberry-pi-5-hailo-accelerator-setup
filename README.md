# raspberry-pi-5-hailo-accelerator-setup

<p align="center">
<a href="https://www.youtube.com/watch?v=xiHv7xd1drY">
    <img width="100%" src="https://raw.githubusercontent.com/computervisioneng/raspberry-pi-5-hailo-accelerator-setup/refs/heads/main/thumbnail.jpg" alt="Watch the video">
    </br>Watch on YouTube: Computer vision on edge | Raspberry Pi 5 AI Kit | Hailo 8L | Object detection
</a>
</p>

## setup instructions

In case you find it useful, here’s a summary of the steps we follow in the video:

**update & upgrade OS**

sudo apt-get update

sudo apt-get upgrade

sudo apt-get install -y build-essential

sudo apt-get install -y raspberrypi-kernel-headers

sudo raspi-config

sudo reboot

**install hailo**

sudo apt install hailo-all

hailortcli fw-control identify

**download examples, install packages**

git clone https://github.com/hailo-ai/hailo-rpi5-examples.git

cd hailo-rpi5-examples

[git checkout tags/25.3.1 -b 25.3.1]

./install.sh

**execution pipeline example**

source setup_env.sh

export DISPLAY=:0

python basic_pipelines/detection.py --input rpi

python basic_pipelines/detection.py --input usb

get-usb-camera

python basic_pipelines/detection.py --input /dev/video<X>

**live example**

enable vnc

install vnc viewer
